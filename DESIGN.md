The main structure of the shelving system is made up of 3 types of part:
* **Side Frames**. Substructures built in square steel tube welded and threaded holes to fit legs and horizontal supports (cross beams). Depending on its position within the set we get three different versions: central, left or right.
* **Cross Beams.** Horizontal pieces that join the sides together and serve as a support for the shelves. Designed in U-shaped folded steel sheet and with welded lids on their heads.
* **Shelves.** Supporting surfaces, designed on 16mm board with two millings on the underside.

Conceptually, the main visual weight of the system resides on the sides, attention is intentionally diverted towards these parts of vertical growth to reduce the attention on the horizontal ones. This is achieved by bringing the perimeter of the side further towards the front side of shelving, while the edge of the shelf and, above all, the face of the cross beam remain in a second and third plane respectively. To reduce even more the visual load of the horizontally developed pieces, the thickness of the shelf is reduced on the two visible edges.

Another key design detail of the system is the absence of visible screws. The open U that shapes the cross beams allows access to the fixing screws, which are hidden once the shelf is supported.

# Modelling
For modelling [Onshape](https://www.onshape.com/) cloud-based parametric CAD system was selected. Despite it's a proprietary software, it has a full feature free license for non-commercial projects in an open-source public work space.

Onshape has implemented a version management system which is compatible with a [gitflow style version management](https://learn.onshape.com/learn/article/gitflow-version-management), so there is a version and history trail in Onshape document with the typical branches that can be found on a Git project: a **master branch** with versions, a **develop branch** where main parts were modelled (side frames, cross beams, shelves and wall fixtures) and where complements should be merged for testing, and several **feature branches** for every complement parts created for shelving system. **Hotfix branches** must be created where necessary.

The entire system was modelled using [Master Model Workflow](https://learn.onshape.com/learn/article/master-model-workflows). This means:
* All critical sketches and dimensions are in the same part studio (master sketches), wich are subsequently inserted into part studios for solid operations (beam, extrude...), so it's easy to identificate errors and/or dimension incoherences between parts.
* Variables were set up for getting consistency. The same variables were defined into those part studios where necessary. Variables must have the same value on every part studio to avoid incoherences between parts.
* In this master model a two-column and six-shelves configuration was used, resulting in a 2100mm high, 2475mm wide and 450mm deep. All STEP, DXF, etc files in file folder were exported from that configuration. In Onshape you can make a copy of the shelving system document and create any configuration by modifying modelling parameters, either by changing variables' values or merely by direct editing dimensions where there isn't variables (suchs as number of shelves or first shelf height) 


## Side frames
Side frames were conceived in S235 steel 25x25mm square tube. This part was modelled using FeatureScript Beams (see [Beams document](https://cad.onshape.com/documents/e15c2c668d138f01242d0c80/v/427e52bd1f3c434d675050e7/e/bd6831589391741e327fec75)).
There are three variations of side frame according to its position on assembly: left, middle and right. This only affects to side holes for joining cross beams, left frame has this holes on its right side, right frame on its left side and middle frame on both sides. In order to simplify document, frame variations were set by means of configurations instead of creating a part studio for each one.
Two M8 tapped holes were placed on the basis in order to place standard stabilising feet. Type and diameter of these feet will depend of weight they must support and floor type.
For shelving configurations where its height were over 800-1000mm is highly recommended to fix the structure to a wall. A wall fixation was developed for that, which can be fastened to a hole on the back side of each side frame.

## Cross beams
 Cross beams are made of 1,5mm thick bended sheet with 4mm thick platin on each head. Sheet metal model was not used intentionally because of there are at least two ways of bending (with or without V-cut), so K-factor must be adjusted according to it.
There are several trims on back cross beam. Their function is to serve as fixation point for cable management by means of strips or elastic cords. If you don't want them, simply suppress all features involved.

## Shelves
In shelves 16mm thick wood board were took into account. A simple extrusion was enough for modelling them. The stepped profile of the bottom allows perfect fit of the shelves between the wings of the cross beams. A tolerance of 0,5mm on vertical surfaces of the fitting was set up.

## Wall fixation
When overall height of shelving system were over 800-1000mm wall fixations should de installed. In side frames' part studio a hole in the back side was sketched, it serves as fixing point for wall fixation: the wider part of the hole allows to insert wall fixation's plate, and the narrower serves height adjusting.

Three parts conform this fixture system: a 2mm-thick plate, an inner bolt and an outer wall fixture. A M5 bolt fixes the plate to the bolt, so when the plate is inserted into the back hole of the side frame and is turned clock-wise, plate and bolt get firmly attached to the side frame. Outer fixture must be fixed to the wall, and fixation between outer and inner pieces is solved by means of two M4 set screws.

If wall fixtures were not necessary, wall fixture-hole operation in side frames' part studio must be suppressed.

# Manufacturing
## Materials
Side frames and cross beams shoud be made of steel. Initially, S235JR steel square tube 25x25x1x5mm side frames were proposed for having adequate resistance. This steel is a type of carbon steel, so it must be applied some type of coating to avoid rust (powder-coating is recommended). Another option to avoid having to give a surface finish is to use stainless steel (AISI 304), although its cost is considerably higher. In cross beams the same material is used, in this case in sheet metal format.

Any type of board derived from wood can be used on the shelves, because of the shelves are not subjected to great mechanically stress -cross beams do almost all the work-. The balance between the desired aspect (wood, colored surface,...) and the associated cost will be the key to deciding between, for example, bare and varnished MDF, veneered or melamine board, or plywood with exposed edge. A determining point in the decision should be the appearance of recessed edges, since the recessed face is also partially visible.

## Processes
Entire shelving system was designed keeping in mind [tube](https://www.youtube.com/watch?v=yF6_DzuoWeI) and [sheet metal](https://www.youtube.com/watch?v=9TjBTG-ShCQ) laser, [sheet metal bender](https://www.youtube.com/watch?v=KJ0b1zkNBxk), TIG welder or [wood board CNC router](https://www.youtube.com/watch?v=3Clo1humDQ0) as manufacturing processes. Las técnicas de fabricación derivadas de CNC aportan una gran precisión en la ejecución, haciendo que los pequeños detalles de encuentros entre piezas queden bien encajados.However, minor changes should be required to adapt design to more conventional manufacturing techniques. 'Classic' manufacturing processes should be suitable as long as that precision can be ensured in the encounters between parts.

Tapped holes in frames and cross beams were modelled directly over tubes and sheets. During manufacturing this joint solution can be replaced by tapped rivets or welded nuts, specially in side frames where tube's face is only 1,5mm thick.
