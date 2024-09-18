# Black Jack in Java
This is a much better, and refined version of my previous implementation of BlackJack in Java. This version has a whole GUI integrated into the framework, with interactable buttons and visuals in the app, to get you closer to the experience of BlackJack like in real life.
There is a plan to make improvements or a separate upgraded version of BlackJack in the near future.

![image](https://github.com/user-attachments/assets/7df8d2de-6a04-4308-8ea6-c127f31fb340)


## Dev Notes

### Card Class:
The Card class represents a playing card with a value (A, 2-10, J, Q, K) and a type (C, D, H, S for clubs, diamonds, hearts, spades).
The getValue() method returns the card's numeric value. Special cases are handled for Ace (11 by default), and face cards (J, Q, K are all worth 10).
The isAce() method checks if the card is an Ace, which is crucial for adjusting scores.
The getImagePath() method assumes a directory structure (./cards/) where card images are stored as value-type.png. Make sure these image files exist.
### Game Flow:
The game begins with the startGame() method, which initializes the deck, dealer hand, and player hand. The deck is built using buildDeck() and shuffled via shuffleDeck().
After dealing two cards to the player and the dealer, players can hit (draw more cards) or stay (end their turn). The dealer must hit until their hand value is 17 or higher.
UI Structure:
The game window uses Swing components: JFrame as the main frame, JPanel for the game board (gamePanel), and another JPanel for the buttons (buttonPanel).
The game board is repainted after every action (hit or stay) to reflect the state of the game visually. Card images are drawn on the board using the paintComponent() method.
