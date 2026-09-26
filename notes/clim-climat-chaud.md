# Une clim, c'est pas un chauffage à l'envers

*septembre 2026*

Quand on apprend le bilan thermique d'un bâtiment, la plupart des cours et des normes viennent d'Europe. Donc on apprend surtout à calculer des **déperditions de chauffage** (EN 12831) : combien de chaleur la maison perd en hiver, pour savoir quelle chaudière mettre.

Au Togo on a le problème inverse. Et la tentation c'est de prendre la même méthode en changeant juste le signe du ΔT. Mauvaise idée, pour au moins trois raisons.

**1. Les apports internes changent de camp.** En hiver, la chaleur des gens et des appareils, c'est un bonus, ça chauffe gratuitement, on peut la déduire (ou l'ignorer par sécurité). En climatisation c'est l'inverse : 10 personnes dans un bureau, les ordinateurs, un frigo, tout ça il faut le sortir. Ça s'additionne. Oublier ça c'est sous-dimensionner.

**2. Le soleil devient le gros morceau.** Un mur ouest à 16 h ou une baie vitrée mal protégée peuvent peser plus lourd que toute la conduction à travers les murs. Il faut calculer la position du soleil selon la latitude, le mois et l'heure, puis le rayonnement reçu par chaque façade. Pour un mur on passe par la température sol-air, pour une vitre par le facteur solaire g.

**3. L'humidité.** À Lomé l'air extérieur est très humide. La clim ne fait pas que refroidir, elle condense de l'eau, et ça coûte de l'énergie (la charge **latente**). Pour la calculer il faut l'humidité absolue, qu'on obtient à partir de la température et de l'humidité relative (formule de Magnus-Tetens).

Sur la paroi elle-même par contre rien ne change, c'est la bonne vieille méthode : R = e/λ pour chaque couche, on additionne avec Rsi et Rse, et U = 1/R.

J'ai mis tout ça dans deux outils :
- [ThermoBat](https://github.com/assakof/thermobat), pour un local, à partir de relevés sur le terrain ([démo](https://assakof.github.io/thermobat/))
- [AkClim](https://github.com/assakof/AkClim), pour un bâtiment entier à partir du plan PDF

Les deux sont testés contre des calculs faits à la main. Prochaine étape pour moi : comparer à des mesures réelles sur des batiments d'ici.
