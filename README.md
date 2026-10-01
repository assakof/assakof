### Salut, moi c'est Ezechiel

Génie énergétique de formation, basé au Togo. J'ai une boutique de réparation (KA Maintenance & Services) et je code surtout les outils dont j'ai besoin moi même : pour l'atelier, pour les calculs de clim, pour le terrain.

Ce que j'utilise le plus : **Python** pour le calcul et le backend, **Flutter / Dart** pour les applis mobiles, un peu de **Kotlin** sur Android. Supabase, FastAPI, SQLite, Qt.

---

### Réalisations

| | |
|---|---|
| **[Atelier de Poche](https://github.com/assakof/atelier-de-poche-app)** | Gestion d'atelier de réparation de téléphones. Fiches, marchandage du prix, étiquettes QR, WhatsApp au client, stock, caisse. Tourne tous les jours dans ma boutique. *Flutter · Android* — [télécharger l'apk](https://github.com/assakof/atelier-de-poche-app/releases/latest) |
| **[Mon Atelier](https://github.com/assakof/mon-atelier-app)** | La même idée pour les métiers de la maintenance : groupes électrogènes, solaire, biogaz, auto, clim... avec rappels d'entretien. *Flutter · Android* — [télécharger l'apk](https://github.com/assakof/mon-atelier-app/releases/latest) |
| **[AkClim](https://github.com/assakof/AkClim)** | Logiciel de dimensionnement thermique : on donne le plan PDF, il sort la charge de clim pièce par pièce. *Python · Qt · Windows* — [installeur](https://github.com/assakof/AkClim/releases/latest) |
| **[ThermoBat](https://github.com/assakof/thermobat)** | Relevé thermique de terrain + calcul de charge, fait pour une présentation de licence. *FastAPI · Flutter Web* — [démo en ligne](https://assakof.github.io/thermobat/) |

Le code de ces projets est privé, mais chaque dépôt a un dossier `extraits/` avec quelques fichiers si vous voulez voir comment j'écris.

### Travaux en cours

- **GeoSmart Field** — appli Android (Kotlin) pour les géomètres et topographes : récepteur GNSS en Bluetooth, corrections RTK via NTRIP, collecte hors ligne sur le terrain. Projet en équipe, je coordonne.
- **Gestion BTP** — plateforme pour l'exploitation d'un bâtiment : pointage sur kiosque avec photo, absences, congés, ordres de mission, maintenance préventive. Flutter + Supabase, marche aussi quand internet coupe.
- **Gestion scolaire** — inscriptions et suivi d'école qui passent par WhatsApp, parce que c'est là que sont les parents. Backend Python.

### Recherche

- **Vectoriser des plans scannés** . Ici beaucoup de plans ne sont que des photos ou des scans de papier. Sans la géométrie, impossible d'automatiser le calcul thermique. Je travaille sur une chaine en vision classique (Python) qui sort les segments de mur d'une image.
- **Charge de climatisation en climat chaud** : adapter les méthodes (ISO 6946, EN 12831, apports solaires sol-air) aux bâtiments et à la météo d'Afrique de l'Ouest, et valider contre des cas réels.

### Publications / notes

Des petites notes que j'écris quand je galère sur un truc ou que j'apprends quelque chose :

- [Pourquoi j'ai codé mon propre logiciel pour ma boutique](notes/atelier-de-poche.md)
- [Une clim, c'est pas un chauffage à l'envers](notes/clim-climat-chaud.md)
- [Compiler une appli Flutter sur un PC de 8 Go avec une connexion qui coupe](notes/flutter-8go.md)

---

Me contacter : WhatsApp 72 04 91 80 / 92 47 78 39
