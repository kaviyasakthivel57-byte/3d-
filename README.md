3D Scatter Plot:

This project visualizes randomly generated 3D points on an HTML5 Canvas using JavaScript. It demonstrates how 3D objects can be rotated using Yaw, Pitch, and Roll angles and displayed on a 2D screen using both Orthographic and Perspective projection techniques. The project also includes interactive controls for rotation and automatic animation.


Project Objective:

The goal is to:
1.Generate random 3D points.
2.Display the points on a 2D canvas.
3.Apply 3D rotations using Yaw, Pitch, and Roll.
4.Compare Orthographic and Perspective projections.
5.Provide an interactive visualization with manual and automatic rotation.

  Project Workflow:
  
The project follows these steps:
1. Generate random 3D coordinates (x, y, z).
2. Store the generated points in **data.json**.
3. Load the data into JavaScript.
4. Convert rotation angles from degrees to radians.
5. Apply Pitch (X-axis), Yaw (Y-axis), and Roll (Z-axis) rotations.
6. Choose either Orthographic or Perspective projection.
7. Convert the rotated 3D coordinates into 2D screen coordinates.
8. Draw the points on the HTML5 Canvas.
9. Continuously update the display for smooth animation.


 Random Number Generation for 3D Points:

  Random values are generated for **x**, **y**, and **z** coordinates.
    Coordinate range:
		
      X: -400 to 400
      Y: -400 to 400
      Z: -400 to 400
			
  The generated coordinates are stored in **data.json** and loaded into the visualization.

Rotation Formulas:

Pitch (Rotation about X-axis):

x' = x
y' = y cos(θ) − z sin(θ)
z' = y sin(θ) + z cos(θ)

Yaw (Rotation about Y-axis):

x' = x cos(θ) + z sin(θ)
y' = y
z' = −x sin(θ) + z cos(θ)

Roll (Rotation about Z-axis):

x' = x cos(θ) − y sin(θ)
y' = x sin(θ) + y cos(θ)
z' = z

These formulas rotate each point around the respective axis before projection.

Degree-to-Radian Conversion:

* JavaScript trigonometric functions (`Math.sin()` and `Math.cos()`) accept angles in **radians**, not degrees.

Formula:

* Radians = Degrees × π / 180

Purpose

* Converts slider values (0°–360°) into radians.
* Enables accurate mathematical rotation calculations.

Orthographic Projection:

* Orthographic projection displays the object without considering depth.

Formula:
  
* x₂D = x
* y₂D = y

Features:

1.No perspective distortion.
2.Objects remain the same size regardless of distance.
3.Used in engineering and technical drawings.

Perspective Projection:

* Perspective projection creates a realistic 3D effect by making distant objects appear smaller.

Formula:

* Scale = f / (f + z)
* x₂D = x × Scale
* y₂D = y × Scale

Where:

1. **f** = Focal length
2. **z** = Depth of the point

Features

1.Produces realistic depth.
2.Objects farther away appear smaller.
3.Commonly used in games and 3D graphics.

Overall Implementation:

* The project is implemented using **HTML**, **CSS**, and **JavaScript**.

 HTML:
1.Creates the webpage.
2.Provides controls for:
  Projection selection
    * Yaw slider
    * Pitch slider
    * Roll slider
    * Auto Rotate option
    * Displays the canvas.

CSS:
1.Styles the webpage.
2.Centers the canvas.
3.Improves the user interface.

JavaScript:

1.Loads 3D point data from **data.json**.
2.Reads slider values.
3.Converts degrees into radians.
4.Applies Pitch, Yaw, and Roll rotations.
5.Performs Orthographic or Perspective projection.
6.Draws the projected points on the canvas.
7.Continuously animates the visualization using `requestAnimationFrame().

Key Features:

1. Interactive 3D point visualization.
2.Random 3D point generation.
3.Real-time Yaw, Pitch, and Roll rotation.
4.Orthographic and Perspective projection modes.
5.Auto-rotation animation.
6.Smooth rendering using HTML5 Canvas.

 Technologies Used:

* HTML5
* CSS3
* JavaScript (ES6)
* HTML5 Canvas
* JSON

Conclusion:

The 3D Scatter Plot Projection System demonstrates the basic concepts of computer graphics, including random 3D point generation, 3D rotation, degree-to-radian conversion, and projection techniques. The project provides an interactive way to understand how three-dimensional objects are transformed and displayed on a two-dimensional screen, making it useful for learning graphics programming and visualization concepts. 

Orthographic:

<img width="1304" height="1021" alt="orthographic" src="https://github.com/user-attachments/assets/c8fc15b2-a1fe-4bc7-b8f0-80e311d28914" />

Perspective:

<img width="1232" height="857" alt="Screenshot 2026-07-04 192238" src="https://github.com/user-attachments/assets/eb0f5ac5-c4cd-46a9-bbea-f62631225030" />





