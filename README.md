# HyperLog

allows you to easily log and graph information about objects in godot

https://youtu.be/tZ3UGLp86l8

examples:

our space-ship has the the following variables:
```
var position = Vector2(10.241, 282.2035)
var direction = Vector2(-1, 0)
var angle = 1.570796
var health_current = 8
var health_max = 12
```
now we can log this information in different ways

`HyperLog.log(ship).text("position:x>round")`

will display the text: position:x 10 

`HyperLog.log(ship).text("position>%0.2f")`

will display the text: position (10.24, 282.20)

`HyperLog.log(ship).text("direction>angle")`

will display the text: direction 3.141593

`HyperLog.log(ship).graph("position")`

will graph out the x and y position of the ship

`HyperLog.log(ship).angle(["direction", "angle"])`

will make an angle-log of the direction and angle

`HyperLog.log(ship).angle("rotation", ship.get_node("gun"))`

will log the rotation of the ship's gun to the panel of the ship

`HyperLog.log(ship).offset(Vector2(200, -20))`

will offset the panel with (200, -20)

`HyperLog.log(ship).align(HALIGN_RIGHT, VALIGN_CENTER)`

will align the panel to the right horizontally and to the center vertically

`HyperLog.log(ship).align(HALIGN_CENTER, VALIGN_BOTTOM).offset(Vector2(0, - 50)).graph("health_current").set_range(0, health_max)`

will display a health graph above the ship

alternatively you can log to the main panel by just accessing the functions directly like:

`
HyperLog.graph("position", ship)
`
