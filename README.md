# blackjackfinite
A modification of openai's blackjack gym, to work with finite size decks. This makes the learning a bit more complicated (you should see a quick jump in quality, followed by a slow but steady rise), but keeps all inputs discrete


To do this, the number of remaining cards (of a specific type) is fed into the reinforcement agent. The Agent is able to play multiple rounds, but as soon as the number of remaining cards is at below 5, it reshuffles the deck. Since the number of possible cards in a deck of 54 cards is huge, multiple cards are summarised into one type. You can modify this by changing the array "numofint". Each entry is equivalent to one group of cards and the standart configuration represents standard Hi-Lo counting. You can also increase the variable "number_of_decks" to increase the maximum number of cards in circulation, but I suggest you leave it as is, since obviously the effects of having only finite cards decrease.


