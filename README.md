# Kinetic Minimalist Pendulum Simulator

An interactive, high-performance pendulum simulator built for the web. This project accurately models the laws of classical physics using a custom-built engine, packaged in a sleek, "Kinetic Minimalist" user interface featuring Glassmorphism. 

Unlike traditional HTML5 web simulations, this project achieves buttery-smooth 60fps animations entirely through dynamically manipulated Scalable Vector Graphics (SVG), requiring **zero external libraries** and bypassing the Canvas API completely.

## ✨ Features

* **Custom Physics Engine:** Utilizes Semi-Implicit Euler integration to accurately calculate orbital mechanics, gravity, friction (damping), and angular acceleration in real-time.
* **Kinetic Minimalism & Glassmorphism:** A modern, distraction-free UI featuring soft gradients, frosted glass panels, and crisp typography.
* **SVG Rendering:** Infinitely sharp vector graphics that look perfect on any screen size or pixel density.
* **Interactive Drag-and-Drop:** Grab the pendulum bob with your mouse or touch screen to naturally set the initial angle and release to start the simulation.
* **Real-Time Telemetry:** Live data readout of the pendulum's current Angle (θ), Angular Velocity (ω), and Angular Acceleration (α).
* **Adjustable Parameters:** Clean sliders allow you to tweak the string length, mass (which dynamically scales the bob's visual volume), and air friction coefficient.
* **Responsive Design:** Automatically adapts to desktop, tablet, and mobile screens.

## 🚀 Getting Started

This project is completely vanilla and self-contained within a single file. There are no build steps, package managers, or local servers required.

1. Download or clone this repository.
2. Locate the `pendulum.html` file.
3. Double-click the file to open it in any modern web browser (Chrome, Firefox, Safari, Edge).

## 🛠️ Technologies Used

* **HTML5:** Semantic structure.
* **CSS3:** Custom properties (variables), Flexbox, CSS backdrops (`backdrop-filter`) for the Glassmorphism effect, and responsive media queries.
* **JavaScript (ES6+):** 
  * Event listeners for mouse and multi-touch interactions.
  * `requestAnimationFrame` for the locked 60fps physics loop.
  * Direct DOM manipulation of SVG attributes.
* **SVG:** Used for rendering the pivot, string, and bob.

## 🧮 Physics Implementation Details

The simulator calculates the motion of a simple gravity pendulum with friction. The core formula governing the angular acceleration (α) is:

α = -(g / L) * sin(θ) - (μ / (m * L²)) * ω

* **g** = Gravity (9.81 m/s²)
* **L** = Length of the string
* **θ** = Current angle
* **μ** = Friction (damping coefficient)
* **m** = Mass of the bob
* **ω** = Angular velocity

## 📝 License

This project is open-source and available under the [MIT License](LICENSE). Feel free to modify, distribute, and use it in your own projects.