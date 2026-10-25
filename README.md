# WS Sounding 🪂

Anciennement PG Soundings. Le nom technique du plugin pour Windy (`windy-plugin-pg-soundings`) ne change pas.

Plugin Windy.com qui affiche, pour un site de vol, un graphique **altitude × heure** pour le vol libre :

- **Vent en altitude** : une flèche par tranche d'altitude et par heure (elle pointe dans le sens où va le vent), colorée selon la vitesse, avec la vitesse en km/h
- **Thermiques** : zone colorée selon la **montée lue au vario** (ascendance au cœur des thermiques moins le taux de chute en spirale, m/s)
- **Qualité des thermiques** de chaque heure, dans l'infobulle : francs, faibles, plafond bas,
  hachés ou très hachés par le vent ; elle n'est pas donnée aux heures de pluie ou de risque
  d'orage
- **Plafond exploitable** (ligne blanche) et **cumulus des thermiques** (tours blanches
  bourgeonnantes, de la base au sommet, aux heures de thermiques exploitables, d'autant plus
  larges que le modèle prévoit de nuages dans leur couche)
- **Nuages d'averses** (tours grises, de la base au sommet, avec un rideau de pluie dessous) quand
  la pluie est faite d'averses, même sans thermiques (nuit, ciel couvert) ; les averses d'heures
  qui se suivent, ou qu'une seule heure sans averse sépare, ne font qu'une masse, d'un seul
  contour, dont la base et le sommet passent par ceux de chaque heure d'averses
- **Plafond nuageux** : la base de la plus basse couche de nuages dense de chaque heure, soulignée
  d'un trait sombre sous l'ombre du dessous du nuage ; la couche elle-même est le voile du modèle
  au-dessus. Base plus sombre et rideau de pluie quand la pluie en tombe (pluie de front). Couche
  de **nuages bas** (stratus, stratocumulus), brouillard quand elle touche le sol, dessus souligné
  de blanc pour une **mer de nuages**. Le trait n'est pas dessiné là où un nuage d'averses traverse
  la couche à la même heure, et s'estompe quand la couche ne dure pas jusqu'à l'heure voisine. Le
  genre de la couche (cumulus, altocumulus, altostratus) se lit dans l'infobulle
- En montagne, tirets là où le **relief est pris dans les nuages**, du sol au niveau des crêtes
  voisines, sauf sous un voile dense qui le montre déjà
- **Ciel de chaque heure** : bandeau « Nuages » au-dessus du graphique, une case par heure où est
  écrite la couverture nuageuse (%), tous étages confondus ; la case va de transparente (ciel
  dégagé) à grise (ciel couvert), de jour comme de nuit
- **Limite pluie-neige** (pointillé pâle) aux heures de précipitations, **virga** (chevrons orange
  sous une averse à base haute, trois chevrons rouges quand l'air très sec peut donner de fortes
  rafales), **ondes de relief** possibles (vague en haut de la colonne) et **tourbillons de
  poussière** possibles (entonnoir au ras du sol)
- **Risque d'orage** heure par heure (surdéveloppement possible, orage probable, orage violent
  possible) et **bandeau d'alerte** les jours d'orage : heure d'arrivée, vitesse de déplacement, rafales.
  Un **orage voisin** (prévu à 55 km et poussé vers le lieu par le vent, quand le modèle n'en prévoit
  pas sur le lieu) a son bandeau, et son icône cerclée de tirets à l'heure où il peut arriver
- **Nébulosité du modèle** à chaque altitude (voile gris, d'autant plus opaque que le ciel y est
  couvert, halo clair en haut pour les nuages plus hauts que le graphique), **isotherme 0 °C**
  (tirets bleus), relief du modèle
- **CAPE et LI heure par heure** : bandeau « CAPE LI » sous la pluie, une case par heure, la CAPE à
  gauche et le LI à droite, chacun sur la couleur de son palier, du vert (stable) au rouge (très
  instable). Le bandeau n'est pas affiché quand les deux restent verts à toutes les heures
- Infobulle au survol : vent, température, vario et nuages à l'altitude pointée, puis plafond
  exploitable, qualité des thermiques, cumulus, vario max, T° au sol (à l'altitude du sol dans le
  modèle), isotherme 0 °C, pluie
- Onglets par jour, choix du modèle (ECMWF, ICON, GFS, ICON-EU, ICON-D2, AROME FR, UKV), altitude max, vue 24 h
- **Heure, altitude et modèle synchronisés avec la carte de Windy**, dans les deux sens : déplacer
  l'heure de la carte change le jour et l'heure du plugin (trait orange sur le graphique, curseur de
  l'heure), et choisir un jour ou une heure dans le plugin déplace la carte. Cliquer ou toucher le
  graphique à une altitude met la carte au niveau le plus proche (sol, 100 m, niveaux de pression),
  repéré sur le graphique par des tirets orange, avec son altitude écrite sur l'axe
- **Lieu synchronisé avec le sélecteur de la carte** (le point de Windy qu'on déplace pour lire le
  vent), sur ordinateur : l'ouvrir ou le déplacer change le lieu du plugin, et cliquer ailleurs sur
  la carte l'y amène. Sur téléphone et tablette, où le sélecteur suit le centre de la carte, le
  lieu ne change qu'en touchant la carte : la déplacer ne le change pas. Le lieu dont le panneau
  affiche la prévision est toujours marqué sur la carte par le repère du plugin, un viseur orange,
  que le sélecteur soit ouvert ou non
- **Lieux favoris** : le nom du lieu, en haut du panneau, ouvre la liste des favoris du compte
  Windy, pour y aller d'un geste ; le cœur à côté du nom ajoute le lieu affiché aux favoris de
  Windy, ou l'en retire
- **Barre de l'heure** en haut du graphique : c'est l'axe des heures, et le bouton orange y porte
  l'heure choisie, au sommet du trait orange qui descend jusqu'au bas du graphique, à travers les
  bandeaux. Il se déplace au doigt ou à
  la souris, d'heure en heure, et la lecture de la journée (▶, dans la marge de l'axe) défile
  d'heure en heure aussi. Au-dessus de l'émagramme, un **curseur** au pas de 5 minutes, avec les
  flèches d'heure en heure et la lecture à ses bouts
- **Vent au sol** : écrit dans le relief brun du graphique, sous la ligne du sol, aux couleurs du
  vent en altitude ; pour chaque heure, le vent moyen (flèche et km/h, « Vent » sur l'axe), puis les
  **rafales** (« Raf. »). Quand le relief est trop mince pour eux, le bas du graphique descend un
  peu sous l'altitude du sol
- Pluviométrie en bas du graphique principal (barres bleues, en mm) : sous chaque heure, la pluie de
  l'heure qui suit. Le bandeau n'est affiché que s'il pleut à l'une des heures affichées
- Survolez une colonne pour voir le détail de l'heure, cliquez dessus pour choisir cette heure et
  cette altitude : l'onglet « Émagramme » montre alors le sondage de l'heure choisie.
  Au doigt, touchez une heure pour la lire, ou gardez le doigt appuyé un instant puis glissez : la
  lecture suit le doigt, sur le graphique comme sur l'émagramme
- **Niveaux du modèle** : des points sur l'axe des altitudes du graphique, et sur les courbes de
  l'émagramme, marquent les niveaux où le modèle fournit ses données. Entre deux points, tout est
  interpolé
- **Émagramme redressé** : altitude en mètres, adiabatiques sèches verticales
  et isothermes obliques, courbe d'état colorée selon la stabilité (rouge : instabilité absolue,
  vert : conditionnelle, clair : stable), avec un point bleu à l'isotherme 0 °C, point de rosée,
  chemin de la particule, adiabatiques saturées et rapport de mélange en fond, zone de formation du nuage (couche claire à sommet
  bourgeonnant, de la base au sommet des cumulus), et à droite la bande des **nuages du modèle** à
  chaque altitude (voile d'autant plus opaque que le ciel y est couvert, trait à la base du plafond
  nuageux de l'heure) puis le vent (flèches dimensionnées par la force) avec la couche convective
  en jaune ; au survol, les valeurs s'écrivent sur les courbes à l'altitude pointée : température,
  point de rosée, particule, et le gradient de température en °C par 100 m, à la couleur de sa
  stabilité
- En option, la **courbe d'état du lever du jour** sur l'émagramme, en trait pâle avec son heure :
  l'écart avec la courbe de l'heure affichée montre ce que la journée a changé (inversion de la
  nuit résorbée, air réchauffé)
- En option, l'**ascension de la particule** sur l'émagramme : son trajet du sol jusqu'où le
  thermique s'arrête (sommet des thermiques, ou du cumulus), son point de rosée en tirets bleus,
  qui la rejoint au niveau de condensation (point étiqueté, atteint ou non), le passage de
  l'adiabatique sèche (jaune) à la saturée (jaune et bleu) à ce niveau, et les zones où elle est
  plus chaude que l'air
- Légendes accessibles par le bouton **ⓘ Légende** de chaque onglet
- **Taille du panneau** au choix, dans les réglages en bas du panneau (bouton « Réglages et
  infos ») : 30, 50, 60 ou 70 % de l'écran (60 % au départ), en largeur sur ordinateur et tablette
  (panneau à droite de la carte), en hauteur sur téléphone (panneau en bas, la carte reste visible
  au-dessus)

L'interface est en français ou en anglais, selon la langue de Windy.

## Données de prévision

Les prévisions viennent de Windy.com, qui sert les modèles de leurs producteurs. WS Sounding les
interpole (au pas horaire, entre les niveaux d'altitude) et en tire ses propres estimations :

- **ECMWF** : modèle IFS, © ECMWF, licence CC BY 4.0
- **ICON, ICON-EU, ICON-D2** : source Deutscher Wetterdienst
- **GFS** : NOAA, domaine public ; la NOAA ne soutient ni n'approuve WS Sounding
- **AROME** : source Météo-France, Licence Ouverte Etalab 2.0
- **UKV** : source Met Office

Le panneau donne la source du modèle choisi dans « Réglages et infos ». Quand Windy ne fournit le
modèle que toutes les 3 heures (compte sans Premium, échéances lointaines), une ligne sous le
graphique le dit et donne les heures que le modèle fournit : les autres sont interpolées.

## Installer le plugin

Sur <https://www.windy.com/plugins>, choisissez « Load plugin directly from URL » et collez :

```
https://windy-plugins.com/2727410/windy-plugin-pg-soundings/1.16.0/plugin.min.js
```

Le plugin signale ensuite lui-même les nouvelles versions. L'historique est dans
[CHANGELOG.md](CHANGELOG.md).

## Données personnelles

Le plugin ne collecte aucune donnée : il n'a pas de serveur et n'envoie rien à WeSoar. Ce qu'il
lit ou écrit passe par Windy :

- **Prévisions, terrain, nom du lieu** : les prévisions, l'altitude du terrain et le nom du lieu
  choisi sont demandés à Windy.
- **Position, à la première ouverture** : quand le plugin s'ouvre sans lieu (ni lieu donné par la
  carte, ni dernier lieu gardé dans le navigateur), il demande la position de l'appareil par la
  géolocalisation de Windy. Le navigateur demande alors l'autorisation, sauf si elle a déjà été
  donnée à windy.com : aucune demande n'apparaît dans ce cas. Sans autorisation, Windy donne une
  position approchée, tirée de l'adresse IP, et à défaut le plugin prend le centre de la carte.
  Cette position devient le lieu affiché ; elle n'est gardée dans le navigateur et écrite dans
  l'adresse de la page qu'arrondie à 0,01° (environ 1 km). Un lieu choisi sur la carte ou dans les
  favoris est gardé tel quel.
- **Dernier lieu** : il est gardé dans le stockage du navigateur (`localStorage`) pour le site
  windy.com, où Windy et ses autres plugins peuvent le lire. Le bouton « Oublier le dernier lieu »
  de « Réglages et infos » l'efface ; le prochain lieu choisi est de nouveau gardé.
- **Favoris** : les lieux favoris sont ceux de Windy. Le cœur de l'en-tête ajoute le lieu affiché
  (son nom et ses coordonnées) aux favoris de Windy, ou l'en retire : Windy l'enregistre dans ses favoris
  et, si l'utilisateur est connecté, dans son compte Windy, d'où le lieu se retrouve sur ses autres
  appareils.
- **Réglages** : la taille du panneau, le thème… restent dans le stockage du navigateur pour
  windy.com, comme le dernier lieu.
- **Nouvelle version** : pour savoir si une version plus récente existe, le plugin interroge au plus
  toutes les 6 heures windy-plugins.com, le site des plugins de Windy.

Aucun site extérieur à Windy ne voit passer l'utilisateur.

## Licence

Code de WeSoar, écrit par Alexandre Pereira, ouvert sous licence [ISC](LICENSE) et diffusé
par WeSoar. Le fichier [NOTICE](NOTICE) dit ce que la licence ne couvre pas : le nom WeSoar et son
logo, qui appartiennent à WeSoar (une version modifiée ne les porte pas), et les fichiers tiers,
qui gardent leurs auteurs et leurs licences (fichiers de configuration et déclarations de types
tirés du modèle de plugin de Windy, Svelte dans la version compilée, police Mona Sans de la page).
Les mentions légales sont au pied de la [page du plugin](https://soundings.wesoar.fr/fr/#legal).

Les valeurs affichées sont des estimations tirées des modèles de prévision, qui peuvent se tromper :
elles ne remplacent ni l'observation du ciel ni les prévisions officielles, et la décision de voler
appartient au seul pilote. WS Sounding est un outil non officiel et non certifié, pour la seule
préparation du vol : ce n'est pas une information météorologique aéronautique officielle (consulter
Météo-France et AEROWEB). L'absence d'alerte d'orage ne signifie pas l'absence de risque, et la
réglementation de l'espace aérien reste à respecter.

## Lancer le plugin en local

1. Installez [Node.js LTS](https://nodejs.org/) (par exemple `winget install OpenJS.NodeJS.LTS`)
2. Dans ce dossier : `npm install` puis `npm start` (compile et sert le plugin sur `https://localhost:9999`)
3. Ouvrez <https://localhost:9999/plugin.js> une première fois et acceptez le certificat auto-signé
4. Allez sur <https://www.windy.com/developer-mode> et chargez le plugin depuis `https://localhost:9999/plugin.js`
5. Ouvrez le plugin depuis le menu (ou par clic droit sur la carte), puis cliquez sur la carte pour changer de site

`npm run build` produit la version finale dans `dist/`. `npm test` lance les tests des calculs
(`tests/`), sur deux prévisions ECMWF réelles enregistrées dans `tests/fixtures/`. Ces prévisions
viennent de Windy, dont les conditions d'utilisation interdisent de redistribuer le contenu : elles
ne sont pas publiées avec le code, et les tests qui les lisent ne passent que là où elles sont.

## Comment sont calculées les estimations

Windy fournit le vent, la température, l'humidité, les nuages et l'altitude géopotentielle des niveaux
de pression (souvent 7 niveaux seulement pour ECMWF : rien entre 850 et 700 hPa, soit ~1 600 m). Le plugin :

- passe les séries au pas horaire si Windy ne donne qu'un pas de 3 h, et suit l'heure locale
  (changement d'heure compris) ; les cumuls de pluie de Windy valent pour la période qui précède
  chaque pas : ils sont recalés sur l'heure qui suit, pour que la pluie tombe sous le nuage qui la donne
- interpole le profil (courbe monotone de Steffen) et le vent (composantes u/v) entre le vent à 10 m
  et les niveaux de pression
- place les **nuages entre deux niveaux** d'après l'humidité : la nébulosité interpolée est réduite
  là où l'air est plus sec que ne le laisse attendre l'humidité des deux niveaux (formule de
  Sundqvist, aucun nuage sous 70 % d'humidité). Sous une inversion, entre un niveau saturé et un
  niveau très sec, le nuage s'arrête où l'air s'assèche, pas à mi-chemin. Aux niveaux du modèle, sa
  nébulosité est gardée telle quelle. Quand un modèle ne fournit la nébulosité d'aucun niveau, elle
  est estimée par la même formule
- estime le **sommet des thermiques** par la méthode de la particule : air mélangé des 500 premiers
  mètres, réchauffé d'une surchauffe qui dépend du flux de chaleur, élevé selon l'adiabatique sèche
  jusqu'à ne plus être plus léger (en température virtuelle) que l'air ambiant
- estime la **base des cumulus** par le niveau de condensation de cette particule (Bolton), puis leur
  **sommet** : la particule saturée suit la pseudo-adiabatique en se mélangeant à l'air ambiant,
  dont l'air sec évapore une partie du nuage et la refroidit ; le sommet est le niveau où elle cesse
  d'être plus légère que l'air. Sans cette dilution, de petits cumulus monteraient jusqu'en haut du
  profil dans un air à peine instable. Le taux de mélange (entraînement) est de 0,2 ÷ rayon du
  nuage, et ce rayon vaut la moitié de la hauteur de la base au-dessus du sol : les thermiques, donc
  les nuages qu'ils nourrissent, sont d'autant plus larges que la couche brassée est épaisse. Il va
  de 0,2 par km (tour d'un kilomètre de rayon, base à 2 000 m du sol ou plus) à 1 par km (petit
  cumulus de 200 m de rayon, base à 400 m ou moins)
- estime **w\*** (vitesse convective de Deardorff) à partir de l'épaisseur de la couche brassée
  (jusqu'à la base des cumulus s'il y en a) et du flux de chaleur au sol : rayonnement par ciel clair
  (Haurwitz), atténué par les nuages (Kasten & Czeplak), réduit sur sol mouillé, divisé par ρ·cp au sol
- donne la **montée au vario** = 1,25 · w\* · profil vertical − 1,1 m/s (taux de chute en spirale) ; le
  profil est à pleine force dès le sol (en relief, les pentes déclenchent à toutes les altitudes)
  puis s'annule au sommet ; le **plafond
  exploitable** est l'altitude où cette montée devient nulle (jamais au-dessus de la base des cumulus)
- signale les **thermiques hachés** : vent moyen de la couche thermique au-delà de 25 km/h,
  **cisaillement** de la couche au-delà de 20 km/h (écart entre le vent au sol et le vent au plafond
  exploitable, en force comme en direction : une brise au sol sous un vent contraire en altitude
  couche et casse les thermiques alors que le vent moyen reste modéré), ou rapport w\* / u\* sous
  2,3 (turbulence mécanique, u\* tiré du vent à 10 m) ; très hachés au-delà de 40 km/h de vent
  moyen, de 35 km/h de cisaillement, ou sous 1,5
- classe la **qualité des thermiques** de chaque heure : très hachés, hachés, sinon faibles (moins
  de +0,5 m/s au vario), plafond bas (moins de 300 m au-dessus du sol) ou, en montagne, plafond
  **sous les crêtes** (il n'atteint pas le niveau des crêtes voisines, voir plus bas : le sol du
  modèle est l'altitude moyenne de sa maille, un plafond peut le dépasser de plusieurs centaines de
  mètres et rester sous le relief), sinon francs. Une heure de pluie (au moins 0,5 mm) ou de
  risque d'orage (surdéveloppement compris) n'est jamais dite « francs » : sa case est grise,
  « pluie ou orage »
- affiche une **CAPE et un LI standard** (air mélangé des 100 hPa les plus bas, sans surchauffe), et
  calcule ceux de l'**air le plus instable** des 300 hPa les plus bas, qui nourrit un orage venu
  d'ailleurs même quand l'air près du sol est stable
- colore la CAPE selon quatre **paliers**, à 200, 650 et 1 600 J/kg : les seuils usuels d'une CAPE
  complète (300, 1 000 et 2 500 J/kg) ramenés à la part que le profil en contient. La CAPE calculée
  s'arrête au dernier niveau fourni (400 hPa) et vaut environ 65 % de la CAPE complète
- estime le **risque d'orage** par deux voies : les cumulus des thermiques (épaisseur, sommet plus froid
  que −20 °C, CAPE standard ≥ 300 J/kg, confirmés par les nuages du modèle), et les orages du modèle
  lui-même à toute heure (CAPE de l'air le plus instable, sommet froid, nuages épais et pluie).
  L'épaisseur et le sommet sont ici ceux que le nuage peut atteindre sans se diluer
  (pseudo-adiabatique pure), plus hauts que le sommet affiché : les seuils d'énergie le supposent
- classe un orage probable en **orage violent possible** quand l'air s'y prête : LI ≤ −6, ou √(2 ·
  CAPE) × cisaillement sol–6 km ≥ 500 m²/s² avec un LI ≤ −2 (la CAPE s'arrête au dernier niveau
  fourni, 400 hPa : ~620 m²/s² sur un profil complet), ou rafales du modèle ≥ 70 km/h
- résume l'**orage du jour** dans un bandeau (8 h – 22 h, heures à venir) : première heure, cause,
  déplacement (vent moyen du sol à 6 km), rafales du modèle, absence de signe l'heure d'avant
- dessine un **nuage d'averses** quand la pluie est faite d'averses. Une heure, prise seule, est
  convective dans trois cas : le modèle annonce des précipitations convectives pour la moitié au
  moins de la pluie de l'heure ; la CAPE standard atteint 50 J/kg sur un nuage d'au moins 2 000 m
  d'épaisseur ; l'air est froid en altitude au-dessus d'un air humide, ce que mesure l'indice des
  totaux (T + Td à 850 hPa − 2 × T à 500 hPa) à partir de 47, ou, là où le niveau 850 hPa est sous
  le sol, un indice de soulèvement d'au plus 2,5. Les averses de traîne, derrière un front froid,
  n'ont presque pas de CAPE : c'est l'indice des totaux qui les repère. La nature de la pluie se
  décide ensuite sur cinq heures, l'heure et les deux de chaque côté : averses si au moins la moitié
  de la pluie y tombe à des heures convectives. Une heure convective minoritaire autour d'elle est
  d'abord écartée, puis celles qui restent entraînent leurs voisines : une énergie qui passe le
  seuil d'un rien ne donne plus une averse isolée au milieu d'une pluie de front. Le nuage dessiné
  est celui de la particule standard, sinon celui de la particule la plus instable ; sans l'un ni
  l'autre, la pluie reste dessinée sous la nappe
- dessine les nuages d'averses d'heures qui se suivent, ou qu'une seule heure sans averse sépare,
  en une masse au contour bourgeonnant
- souligne la base du **plafond nuageux** de chaque heure, sa plus basse couche de nuages dense :
  la couche de nuages bas s'il y en a une (voir plus bas), sinon la plus basse couche continue où
  la nébulosité du modèle atteint 50 %, à n'importe quelle altitude, de l'altitude où elle dépasse
  40 % à celle où elle y retombe. Mesurée à 40 %, la base ne saute pas d'un niveau à l'autre quand
  la nébulosité oscille autour de 50 %. La couche naît à 50 % et se prolonge d'heure en heure tant
  qu'elle garde 40 % à la même altitude : une autre couche, plus basse ou plus haute, qui n'a
  jamais atteint 50 %, ne prend pas sa place. Deux heures voisines portent la même couche quand
  leurs altitudes se recouvrent, à 250 m près ; sinon ce sont deux couches, et le long d'une même
  couche, base et sommet sont lissés avec les heures voisines (moyenne sur trois heures) : ils
  sautaient d'un niveau du modèle à l'autre quand la nébulosité oscille autour du seuil. Seule la base est
  dessinée : la couche elle-même est le voile du modèle, léger jusqu'à 40 % de nébulosité et
  plein dès 75 %, et son sommet s'y perd
- quand la pluie n'est pas faite d'averses, elle tombe de cette couche, à la base plus sombre
  (**pluie de front**, bruine). Sans couche dense, elle garde la plus basse couche continue où la
  nébulosité atteint la moitié de sa plus forte valeur
- dessine une **couche de nuages bas** (stratus, stratocumulus) quand la plus basse couche continue à
  50 % de nébulosité a sa base à moins de 2 000 m du sol et son sommet à moins de 3 000 m (plus
  épaisse, c'est une masse nuageuse de front). Elle naît à 50 % et se prolonge d'heure en heure tant
  qu'elle garde 40 % à la même altitude. Elle touche le sol (**brouillard**) quand l'air y est saturé (T − Td ≤ 0,5 °C)
  et qu'elle commence à moins de 300 m. C'est une **mer de nuages** quand elle couvre au moins 70 %
  du ciel sous un air clair (20 % de nuages au plus) et sec (T − Td ≥ 5 °C) au niveau du modèle
  juste au-dessus. Base et sommet sont interpolés entre deux niveaux du modèle : ils ne sont justes
  qu'à quelques centaines de mètres près quand ces niveaux sont espacés
- donne le **genre** d'une couche quand le profil le dit, écrit dans l'infobulle. Une couche de
  nuages bas est une **couche de cumulus** (cumulus, stratocumulus) quand des thermiques
  exploitables montent jusqu'à elle, à 300 m près ; sans thermique, le profil ne sépare pas le
  stratus du stratocumulus : elle reste « nuages bas ». Une couche sans pluie dont la base est à
  l'étage moyen (à plus de 2 000 m du sol, sous 450 hPa) est un **altocumulus** si elle fait moins
  de 2 000 m d'épaisseur ; plus épaisse, c'est un **altostratus** ou un altocumulus épais.
  L'altocumulus castellanus, signe d'instabilité en altitude, n'est pas repéré
- marque de tirets le **relief pris dans les nuages** : là où T − Td ne dépasse pas 1,5 °C sur au
  moins 100 m, l'air condense dès qu'une pente le soulève de moins de 200 m, que le modèle y annonce
  une couche ou non. Les tirets ne vont que du sol au **niveau des crêtes voisines** : le plus haut
  de 24 points du terrain lus auprès de Windy sur trois cercles de 3, 6 et 10 km, s'il dépasse d'au
  moins 300 m le sol du modèle. Les sommets passent entre ces points : c'est un niveau de crêtes,
  pas le plus haut sommet. En plaine, rien n'est dessiné ; le versant au vent n'est pas connu
- place l'**isotherme 0 °C** au plus haut niveau où l'air repasse au-dessus de 0 °C. Sous une
  inversion (gel au sol, air plus doux au-dessus), c'est le sommet de la couche douce, pas le sol ;
  quand il gèle sur toute la colonne, c'est l'altitude du sol
- trace la **limite pluie-neige** aux heures de précipitations : l'altitude au-dessus de laquelle
  le thermomètre mouillé reste sous +1 °C, où les flocons ne fondent pas. Elle est cherchée depuis
  le haut du profil, et vaut l'altitude du sol quand la neige l'atteint
- signale une **virga** quand la base d'un nuage d'averses, ou des cumulus d'une heure de
  surdéveloppement ou d'orage, est à plus de 1 500 m du sol : l'air est alors sec dessous (au moins
  12 °C entre température et point de rosée au sol), la pluie s'y évapore et le refroidit. Elle est
  dite **forte** (trois chevrons rouges) quand la descente de cet air a beaucoup d'énergie : l'air
  pris à la base du nuage, refroidi jusqu'à son thermomètre mouillé, descend le long de la
  pseudo-adiabatique jusqu'au sol, et l'énergie de cette descente (DCAPE) atteint environ 400 J/kg,
  soit une vitesse théorique √(2 · DCAPE) de 100 km/h. Cette vitesse est un maximum théorique : elle
  sert de seuil, pas de rafale annoncée, et ce seuil n'est pas vérifié sur des observations
- signale des **tourbillons de poussière** possibles quand leurs ingrédients sont réunis : w\* d'au
  moins 2,5 m/s, couche convective d'au moins 1 500 m, rapport w\* / u\* d'au moins 5 (convection
  libre, −zi/L ≥ 50 : le vent au sol reste faible devant les thermiques), au moins 10 °C entre la
  température et le point de rosée au sol, moins de 1 mm de pluie dans les 24 heures et l'heure, et
  moins de 30 % du ciel qui cache le soleil. Seuils tirés de la littérature : aucune observation de
  tourbillons ne permet de les caler
- montre le **ciel de chaque heure** dans le bandeau « Nuages » : la couverture nuageuse totale
  (maximum de chaque étage, bas, moyen et haut, puis recouvrement aléatoire entre étages). Le
  calcul des thermiques, lui, compte la part qui cache le soleil, où les nuages bas comptent en
  entier, les nuages moyens pour 70 % et les nuages hauts pour 30 % : c'est elle qui atténue le
  rayonnement. Les **étages** se comptent depuis le sol : bas à moins de 2 000 m du sol, haut à
  partir de 450 hPa (nuages de glace), moyen entre les deux. L'opacité d'un niveau passe sans
  marche de 100 % à moins de 1 500 m du sol à 70 % à plus de 2 500 m. La hauteur d'un niveau est
  celle de sa pression dans l'atmosphère standard, la même à toute heure. Avec une limite fixe à
  700 hPa, l'étage bas ne faisait plus que 1 000 m au-dessus d'un site à 2 000 m. Sous 500 m
  d'altitude, rien ne change
- nomme **bruine** une pluie de moins de 0,5 mm/h qui tombe d'une couche de nuages bas, sans averse,
  et **cumulus étalés** des cumulus dont la couche (de 200 m sous la base à 200 m au-dessus du
  sommet) contient au moins 60 % de nuages du modèle
- signale des **ondes de relief** possibles au-dessus des crêtes voisines : vent d'au moins 30 km/h
  à leur niveau, qui tourne de moins de 30° sur les 4 000 m au-dessus, dans un air stable dont le
  paramètre de Scorer (stabilité ÷ carré du vent) est au moins deux fois plus fort dans les 1 500
  premiers mètres que plus haut. L'orientation des crêtes n'est pas connue : c'est un signal
- dessine les cumulus des thermiques d'autant plus larges que le modèle prévoit de nuages dans
  leur couche : la moitié de la colonne à 10 % de nébulosité ou moins, les quatre cinquièmes à
  60 % (cumulus étalés)
- trace la courbe d'état de l'**émagramme** en gardant l'air surchauffé près du sol. Entre le point
  à 2 m et le premier niveau de pression, souvent 300 à 500 m plus haut, le modèle ne donne rien :
  reliés tels quels, ils dessineraient une instabilité absolue sur toute cette épaisseur. Quand le
  sol est plus chaud que l'adiabatique sèche qui passe par le premier niveau, la courbe rejoint
  cette adiabatique à 100 m du sol (au tiers de l'écart s'il est plus mince), puis la suit jusqu'à
  ce niveau, comme dans une couche brassée par la convection. Seul le tracé change : les calculs
  (sommet des thermiques, plafond, CAPE) gardent le profil du modèle
- ne montre les **cumulus des thermiques** (graphique, infobulle) qu'aux heures de
  thermiques exploitables : dans un air saturé, sous un ciel couvert, la particule condense encore
  et son « nuage » peut faire plusieurs kilomètres d'épaisseur sans qu'aucun thermique le nourrisse.
  L'émagramme, lui, montre toujours l'ascension de la particule
- signale un **orage voisin** : en plus de la prévision du lieu, il charge celle de quatre points
  voisins, à 55 km au nord, au sud, à l'est et à l'ouest. Un de ces points porte un risque d'orage
  (orage probable ou orage violent possible) entre 8 h et 22 h, le vent qui déplace l'orage (vent
  moyen du sol à 6 km, au moins 10 km/h) pointe vers le lieu à 45° près, et le modèle ne prévoit
  pas d'orage sur le lieu entre l'heure de cet orage et 2 heures après son arrivée. L'heure
  d'arrivée est la distance divisée par la vitesse dans la direction du lieu

Ce sont des **ordres de grandeur**, pas des mesures. Ils ne remplacent ni un vrai modèle
aérologique ni l'observation sur le terrain.

Le code est dans `src/` : `plugin.svelte` (interface, chargement), `Chart.svelte` (graphique),
`Emagram.svelte`, `physics.ts` (calculs et couleurs), `interpolate.ts` (pas horaire), `time.ts`
(heure locale), `nearby.ts` (orages voisins), `relief.ts` (crêtes voisines), `level.ts` (altitude
de la carte), `scrub.ts` (lecture au doigt).
