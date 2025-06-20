
# mapcompare2d

`mapcompare2d` is a highly portable program for viewing different maps of a 2D planar world in real time.

# usage
## toolbar
The toolbar contains different tools:
- #### Move tool
	Enters `Drag mode`. Shortcut key is `M`.
- #### Line tool
	Enters `Line mode`. Shortcut key is `L`.
- #### Brush tool
	Enters `Draw mode`. Shortcut key is `B`.
- #### Change view
	These buttons change the view mode of maps. When a map is in an alternative view mode, coordinates of another map are projected onto it instead of its own. **Can result in bad performance depending on the complexity of transformations being used, and amount of lines visible.**
## maps
Maps can be interacted with the following:
- ### scrollwheel:
	Scrolling can zoom in and out of a map. The center of the zoom is at the cursor.
- ### left mouse button:
	The left mouse button does different things depending on the `mode`
	- #### Drag mode
		In this mode, maps can be dragged around with the left mouse button. 
	-	#### Line mode
		In this mode, a 2D planar world line can be placed on maps. The start point is where the left mouse button was pressed, the end point is where it was released.
	- #### Draw mode
		In this mode, a line is placed between the start and endpoint of any mouse movement while the left mouse button is held down.
## coordinate transformations
Above each map are 2 textboxes and a button. The textboxes top to bottom are for:
- #### real world coordinates => map coordinates function
	Converts real world coordinates to map coordinates.
- #### map coordinates => real world coordinates function
	Converts map coordinates to real world coordinates.
### syntax
The syntax for transformation functions is the following: ***(x1; x2) => (f<sub>x1</sub>(x1, x2); f<sub>x2</sub>(x1, x2))*** where
***x1*** and ***x2*** are alphanumerically named variables
 ***f<sub>x1</sub>(x1, x2)*** and ***f<sub>x2</sub>(x1, x2))*** are expressions made up of ***x1***, ***x2***, mathematical operations and functions.
 This defines a function mapping a set of all points to another set of points.

The button updates the map to use the inputted transformation functions. **Making them nonsensical or not inverses of one another can result in strange behavior.**

# project status

 The project itself is a html/javascript port of a university assignment I originally wrote using C++/OpenGL. I plan on expanding this project. Currently, this project is early into development, and is expected to receive frequent updates.