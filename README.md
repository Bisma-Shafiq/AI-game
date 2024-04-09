# AI-game

It's a simple game that uses hand gestures to play rock-paper-scissors against an AI opponent. Each part of the code is responsible for a specific aspect of the game, such as hand detection, game logic, and user interface.
**Importing Libraries:**

The code begins by importing necessary libraries. random is used for generating random numbers, cv2 is OpenCV library for image processing, and cvzone is a library built on top of OpenCV providing additional functionalities. The HandDetector class is imported from cvzone.HandTrackingModule to detect hand gestures.

**Initializing Variables:**

Variables like cap, detector, timer, stateResult, startGame, and scores are initialized to manage game state, timer, and scores.

**Processing Webcam Feed:**

The webcam feed is captured and resized to a smaller size for faster processing. The region of interest (ROI) is extracted from the resized frame.

**Hand Detection:**

The findHands() function from the HandDetector class is used to detect hands in the ROI. It returns a list of detected hands and an image with visualizations of detected hands (if any).

**Game Logic:**

If the game has started (startGame is True), the code proceeds to play the game. It checks if enough time has passed since the game started (timer > 3 seconds), then proceeds to determine the player's move based on hand gestures.

**AI Move:**

Once the player's move is determined, the AI randomly selects its move (rock, paper, or scissors).

**Determining Winner:**

The player's move and AI's move are compared to determine the winner of the round. Scores are updated accordingly.

**Displaying Results:**

The scores are displayed on the screen along with the webcam feed and any necessary overlays.

**User Input Handling:**

The program listens for user input. If the 'q' key is pressed, the game starts, and the timer is initialized. If the 'x' key is pressed, the program exits.
