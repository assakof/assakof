# Compiler une appli Flutter sur un PC de 8 Go avec une connexion qui coupe

*septembre 2026*

Petit pense-bête, si ça peut servir à quelqu'un dans la même situation que moi : Windows, 8 Go de RAM, connexion par partage mobile, et un vrai téléphone Android branché en USB (un émulateur sur 8 Go, oubliez).

**Pas besoin d'Android Studio.** Les « command line tools » du SDK Android suffisent. On installe avec `sdkmanager` ce qu'il faut (platform, build-tools), on accepte les licences avec `flutter doctor --android-licenses` et c'est bon.

**Gradle prend toute la RAM.** Le projet Flutter généré met `-Xmx8G` dans `android/gradle.properties`. Sur une machine de 8 Go, tout le PC se fige. J'ai mis :

```
org.gradle.jvmargs=-Xmx2048M -XX:MaxMetaspaceSize=1G
```

Plus lent, mais ça passe.

**Le NDK qui se télécharge pendant le build.** Mon premier build a planté après plus d'une heure parce que la connexion a coupé en plein téléchargement du NDK. La solution : le télécharger à part avant, avec `sdkmanager "ndk;<version>"` (et `cmake` pareil), comme ça si ça coupe on relance juste ce téléchargement, pas tout le build.

**Kotlin qui plante : « different roots ».** Mon cache pub était sur C: et le projet sur E:. Le compilateur Kotlin incrémental n'aime pas du tout ça sous Windows et plante en fermant ses caches. Une ligne dans `gradle.properties` règle le problème :

```
kotlin.incremental=false
```

**L'APK de 73 Mo.** Avec la lecture des QR codes (MLKit) l'apk universel est énorme. En séparant par architecture :

```
flutter build apk --release --split-per-abi
```

on tombe à environ 25 Mo pour la version arm64, celle qui va sur presque tous les téléphones récents.

**Et le permission INTERNET.** En debug tout marche, en release plus rien ne se connecte. Il manquait `<uses-permission android:name="android.permission.INTERNET"/>` dans le `AndroidManifest.xml` principal. Classique, mais on s'est tous fait avoir une fois.
