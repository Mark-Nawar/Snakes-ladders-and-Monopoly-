# Snakes-ladders-and-Monopoly-


A OOP class project were the rules of object oriented programming are used to implement the game's stucture.


<h2>Game description</h2>
<ul>
<li>4 players will compete to reach the cell 99 on the grid with all of them starting from cell 1
 <li> snakes get you down ladders get you up and cards can be your friend or your worst enemy
  <li> players start the game with 200 coins in their wallets and every three dice rolls the player don't move on the grid but get his wallet charged by 10*dice_value
</ul>

<h2> The Cards rules</h2>
<ul>
  <li> Card1: DecWalletCard:
. Decrements the current player’s wallet by a value specified in grid design time.
.Input data during grid design time:

<li> Card2: NextCard:
. Moves the current player forward to the start of the next game object of a chosen type
(ladder, snake, coin set or cards).
. If no game objects of this type in the cells after the player to the grid end cell, then the
cells before the players are searched starting from the first grid cell to the player
position.
. If no game objects of this type exist, then do not move.
. Input data during grid design time:
. A number indicating the game object type to move to (1 means ladders, 2
snakes, 3 coin sets, 4 cards).

<li>Card3: BackwardCard:
. Move all other players backward the same number of steps that the current player just
rolled (if they reach a ladder, snake or coins at the end of moving, take it).

<li> Card4: PreventCard:
. Prevents one of the other players from rolling the next turn.
. When a player gets this card, he should choose the one other player that will be
prevented from rolling by clicking on the cell he is currently in.
. This can be handled as getting a value of zero instead of a dice roll. This means that the
cancelled turn counts normally towards recharge the wallet turn.
. Input data during game time:
. The cell of the player to be prevented from rolling (by clicking on the cell not
entering the cell number).

<li> Card5: FireCard
. Fires all other players that are currently located at the same row or same column of the
card by moving them to the start cell of the grid (cell number 1) and decrementing their
wallets by half their current value.

<li> Card6: FreezeCard:
. Freezes the other players that are currently in odd/even cells for a specific number of
turns by making them don’t move nor recharge their wallets.
. Input data during grid design time:
. A boolean indicating odd cells or even cells should be frozen.
. Input The number of turns to freeze.
<li> Card7 to Card11: MonopolyCards [5 Cards]:
. Monopoly cards are five cards; each represents a city:
Cairo, Alex, Aswan, Luxor and Hurghada.
. The same city may exist in many cells in the grid.
. Those five cards give the player the option to buy a specific city with all its cells. For
example, if a player chooses to buy Alex, he will own all cells having a card Alex.
.Each city has a price to be bought with and fees for any players passes by the cell.
. The city price is deducted from the player’s wallet in case he chooses to buy the cell.
. Whenever a player moves to a city owned by another player, he has to pay fees to
owner.
. Input data during grid design time:
.Input City price
.Input Fees to be paid by passing players
<li> Card12: TakeCityCard:
. Enables the current player to choose one city to take for free either from not bought
cities or from the cities bought by other players.
. Input data during game time:
.Input The name of the city the player chooses to take

<li> Card13: LoseCityCard:
. Makes the current player lose the maximum-price city of his owned cities.
. If the maximum-price city is mortgaged to another player, then the player who got the
LoseCityCard loses his ability to return this city and its ownership goes permanently to
the player who mortgaged it.
<li> Card14: ReturnMortgagedCard:
. Makes the current player return the city that has the minimum price in his mortgaged
cities.
. The current player gets this city back for free and the player that the city was mortgaged
to does NOT take his money back.

<li> Card15: BenefitAllCard:
. Makes the current player take the benefit (the fees) of all the bought cities for a specific
number of turns even if he is not their owner.
. The players who owned those cities don’t take their fees for this specific number of
turns.
. Input data during grid design time:
.Input The number of turns by which we switch the benefit, for example, if the number
of turns is 3, then the benefit switch will be held for the next 3 dice rolls of the
current player.
  </ul>
