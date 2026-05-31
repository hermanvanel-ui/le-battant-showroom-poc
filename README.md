# Le battant — showroom 3D des 8 volets

POC du concept Herman 2026-05-31 : page `/gammes` V2 transformée en **showroom 3D immersif**. Hero (volets s'ouvrent au scroll) → caméra entre dans la pièce → 8 volets disposés sur piédestaux → caméra fait le tour, specs apparaissent à chaque arrêt.

## Live

<https://hermanvanel-ui.github.io/le-battant-showroom-poc/>

## Les 8 volets

| # | Modèle | Géométrie | Couleur alu |
|---|---|---|---|
| 01 | Battant à gond | 2 panneaux ouverts 55° | vert-volet |
| 02 | Battant à dormant | 2 panneaux ouverts 40° | crème |
| 03 | Pliant | 4 panneaux accordéon | vert-volet |
| 04 | Pliant suspendu | 4 panneaux accordéon | noir |
| 05 | Coulissant suspendu | 2 panneaux + rail haut | vert-volet |
| 06 | Brise-vue | cadre + lamelles fixes 60° | crème |
| 07 | Brise-soleil | cadre + lamelles 25° | vert-volet |
| 08 | Séparatif balcon | panneau plein cadre noir | rouge sang |

## Stack

- **Three.js** 0.166 + Lenis 1.1.13 smooth scroll
- **EffectComposer + UnrealBloomPass** (post-process)
- **HDRI Polyhaven** : `industrial_sunset_02` (atelier dramatique)
- **Textures PBR Polyhaven** : `concrete_floor_02` (sol), `painted_plaster_wall` (murs), `worn_planks` (piédestaux), `metal_plate_02` (réserve métal)
- **MeshPhysicalMaterial** : 4 variantes alu (vert-volet, crème, noir, rouge)
- 11 waypoints camera path (Catmull-Rom centripetal)
- 8 spots LED dédiés (1 par volet) + ambient HDRI

## Concept

Cf. brain Herman → `Idées d'évolution du système.md` § *Showroom 3D Le battant* + journal 2026-05-31 capture #8.

→ **Argument de vente massif** : aucun concurrent menuiserie alu (Technal, Reynaers, Schüco, Bubendorff, Franciaflex) n'a un showroom 3D au scroll. C'est la signature qui justifie un positionnement premium pour Simon, et qui devient un argument de prospection pour vendre d'autres sites de fabricants ensuite.

## TODO

- [ ] Vraie texture alu brossé via Polyhaven (au lieu des MeshPhysical color-only)
- [ ] Mini-animation d'ouverture par volet quand la caméra arrive
- [ ] Sons subtils (cliquetis paumelles, glissement coulissant)
- [ ] Intégration dans la V2 Le battant `/gammes`
- [ ] Variantes 2k textures pour desktop
