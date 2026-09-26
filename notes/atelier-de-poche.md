# Pourquoi j'ai codé mon propre logiciel pour ma boutique

*septembre 2026*

Dans une boutique de réparation de téléphones, la journée ressemble à ça : un client arrive avec un écran cassé, on discute le prix, on se met d'accord, on range le téléphone quelque part, et on note tout dans un cahier. Trois jours après le client revient, et là il faut retrouver le téléphone, retrouver le prix convenu, et se souvenir si il a déjà donné une avance.

Le cahier marche... jusqu'au jour où il ne marche plus. Une page arrachée, une écriture illisible, un technicien qui a noté ailleurs.

J'ai regardé ce qui existait. Il y a de bons logiciels (RepairDesk et compagnie), mais ils sont faits pour l'Europe ou les États-Unis : paiement par carte, prix fixes, abonnement en dollars, et il faut internet en permanence. Chez nous :

- **le prix se négocie**. Le patron a un prix plancher dans la tête, le client propose, on tombe d'accord quelque part. Aucun logiciel que j'ai vu ne gère ça
- on paye en espèces, T-Money, Flooz
- le réseau coupe, souvent
- les clients, on les joint sur WhatsApp, pas par e-mail

Alors j'ai fait Atelier de Poche. Quelques choix que je referais pareil :

**Pas d'API WhatsApp payante.** L'appli ouvre WhatsApp avec le message déjà écrit (« votre téléphone est prêt, montant à régler : 15 000 FCFA ») et le technicien appuie juste sur envoyer. Zéro frais, aucun risque que le numéro de la boutique soit bloqué.

**Une étiquette QR sur chaque téléphone**, avec l'endroit où il est rangé. Quand le client revient on scanne, on sait que c'est dans l'armoire 2, deuxième étagère. Ça a l'air de rien mais ça fait gagner un temps fou.

**Hors connexion d'abord.** L'appli écrit d'abord sur le téléphone et envoie au serveur quand le réseau revient. Les tickets créés sans réseau ont un numéro différent (R-L0007 au lieu de R-0007) pour ne jamais avoir deux fois le même numéro, parce qu'une fois l'étiquette imprimée on ne peut plus la changer.

**Le Pro se paye en Mobile Money.** Beaucoup de patrons n'ont pas de carte bancaire, donc pas de Google Play. Ils payent, je leur donne un code, ils l'entrent dans l'appli.

Le plus dur au final ça n'a pas été le code, ça a été de comprendre exactement comment on travaille dans une boutique. Et ça, j'avais l'avantage d'être dedans tous les jours.

→ [Atelier de Poche](https://github.com/assakof/atelier-de-poche-app)
