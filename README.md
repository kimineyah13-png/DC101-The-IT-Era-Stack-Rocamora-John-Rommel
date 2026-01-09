I.  Project Architecture (The "IT Era" Stack)

	1.	Open (VS) VISUAL STUDIO

2.index.html (The Structure): This acts as the skeleton of your application. It defines the Canvas API element, which is the "screen" where the game is rendered. It also links the CSS for styling and the JavaScript for logic.
 
	3.	style.css (The Presentation): This provides the "Cyberpunk/Modern IT" aesthetic. It uses a dark palette (#1a1a2e) to reduce eye strain (a common UI/UX practice in the IT era) and centers the game for a professional look.

	4.	script.js (The Logic): This is the "brain" of the game. It handles the movement physics, collision math, and the game loop that refreshes every 100 milliseconds.

	5.	assets/ (The Resources): This folder is reserved for external media like sound effects (e.g., a "beep" when eating) or background music, which adds immersion to the user experience.


II. Step-by-Step Game Mechanics

Here is how the game actually functions during runtime:

	1.	Grid Initialization: The game world is divided into a grid of squares (20×20 pixels each). This "box" unit ensures that the snake and food always align perfectly.

	2.	Snake Array: The snake is stored as an Array of Objects. The first object in the array is the "Head," and the following objects are the "Body."

	3.	The Game Loop (setInterval): The draw() function runs repeatedly. Every 10th of a second, it clears the previous frame and draws the new positions of the snake and food.

	4.	Input Handling: An Event Listener "listens" for your keyboard presses. It prevents the snake from turning 180° into itself (e.g., if you are moving Left, you cannot immediately press Right), which prevents instant self-collision.

	5.	Food Generation (Math.random): When the game starts or food is eaten, the script generates a random X and Y coordinate. It uses Math.floor to ensure the food stays exactly within the grid lines.

	6.	Movement Logic: * The script calculates the new position of the head based on the current direction.

It adds a "new head" to the front of the array.

If the snake did not eat food, it removes the last piece of the tail using .pop(). This creates the illusion of movement.

	7.	Collision Detection:

Wall Collision: If the head’s X or Y coordinates go below 0 or above the canvas width/height, the game stops.

Self-Collision: A loop checks if the new head's coordinates match any of the coordinates in the body array.

	8.	Score Management: Every time the head's coordinates match the food's coordinates, a global score variable is incremented and updated on the screen in real-time.


III.

This code is a practical example of ICT in Education. By building this, you are demonstrating:

Logical Thinking: Translating human rules (Snake) into machine language.

Web Development Skills: Understanding how HTML/CSS/JS interact.

Resource Management: Organizing files and folders efficiently for a digital project.

## Instructions to Run the Game

1. Install Git (if not already installed):  
   Download and install Git from https://git-scm.com

2. Clone the repository:
   ```bash
   git clone https://github.com/kimineyah13-png/DC101-The-IT-Era-Stack-Rocamora-John-Rommel
