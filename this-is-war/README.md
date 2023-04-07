# This is War
Simple implementation of the classic card game War.

**Live version here**: https://jmart2210.github.io/this-is-war/

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, & Deck of Cards API

The Deck of Cards API request happens at page load. The deck is distributed evenly between each player as an array. Each round the top card is drawn from the hands and compared. The player with the higher card takes the pot. If the initial cards are equal, a "war" ensues, increasing the stakes. Instead of just pushing the pot to the back of the winning player's hand, I chose to give each player a "wins" pile separate from their hand. Currently there is no benefit to doing it this way, but there are a number of optimizations I could make that would make use of the additional architecture. 

## Optimizations:

* The UI is bare bones. I could add some animations with cards going to/from the hand, playing field, then the winning pile. And some logic so the deck visually shows how well they are doing. Currently the meter serves as a rough indicator.

* Shuffle each round: War tends to be a drawn out game, I could shuffle the winning pile before returning it back to the player's hand to allow for a little variety.

* Implement some kind of round system, so users can play to some conclusion.

<img src="warExample.gif">