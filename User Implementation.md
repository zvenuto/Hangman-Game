Image of UML Diagram:
![image](https://github.com/user-attachments/assets/95e2869a-4e97-4fb6-a6dc-8aef94169729)

The diagram consists of 3 main classes:
- HangmanApp
- HangmanGame
- WordBank

HangmanApp consists of all the code for the JavaFX GUI. It is the reason the application is able to open as a graphical interface.
HangmanGame consists of all the code to get the application to actually work and be playable. It is the main class that allows the user to play the game.
WordBank consists of all the words that could be randomly selected to be playable in the game. This class also breaks up the words between easy, medium, and hard. 

Class structure and UML explanation:

HangmanApp Class:
- Label displayWordLabel: Displays the dashes and correctly guessed letters.
- Label remainingAttemptsLabel: Displays the number of remaining attempts the player has.
Label incorrectGuessesLabel: Displays the incorrect guesses that the player has already guessed.
TextField inputField: Displays an interactable text field that allows the player to input their letter guess.
Button guessButton: Displays an interactable button that allows the player to submit their letter guess.
Label gameOverLabel: Displays a game over message when the player wins or loses. 
+void start(Stage primaryStage): Initializes the GUI
+void startNewGame(String difficulty): Starts a new game based on the difficulty level the player selected.
+void processGuess(): Processes the player's letter guess and updates the GUI based on whether the guess was correct or incorrect.

HangmanGame Class:
String getDisplayWord(): Keeps track of the word and the correctly guessed letters.
String getIncorrectGuesses(): Keeps track of the incorrect guesses the player made.
int getRemainingAttemtps(): Keeps track of the amount of remaining guess attemtps.
String getWordToGuess(): Keeps track of the word that needs to be guessed.
boolean guessLetter(char guess): Checks if the guessed letter the player makes is in the word.
boolean isGameWon(): Keeps track if the player won the game.
boolean isGameLost(): Keeps track if the player lost the game.
+void resetGame(String difficulty): Resets the game based on the difficulty level the player selected.

WordBank Class: 
List<String> words: Provides a list of words that the application randomly selects out of for the game. 
+void addWord(string word): Add a new word to the word pool.
+void getRandomWord(): CHooses a random word from the word pool for the game.

