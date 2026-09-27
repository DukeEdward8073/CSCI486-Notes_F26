
Recall that we are doing search with two players one max and one min
they well attempt to have their best possible score ensuring that the other player does not get their best outcome

Alpha-Beta pruning pseudo code from previous class time

![[Pasted image 20260916111639.png]]


Game playing formats we do not know how to handle
	infinite game trees
	more than 2 players
	games w subjective goal states
	randomness
	non-zero-sum games


focus on
	more than 2 players
		add a level for each player
		record utilities separately
	non zero sum
		keep track of utilities separately for each player making sure that each player maximizes their utility
randomness/ stochastic games
	chance gets its own turn
	![[Pasted image 20260916112709.png]]
	but does not have any utility of its own because it is random chance
	average case
	probability ranges from 0-1
	d6 example
		1 wp 1/6
		2 wp 1/6
	loaded coin
		H wp 60%
		T wp 40%


expectimax
example of starter tree for random
![[Pasted image 20260916113120.png]]


expected value: sum of probability of number occurring times number

tree with expected values
	![[Pasted image 20260916113733.png]]

can't prune because all chance values have an effect on the outcome

infromed search/pruning using domain knowledge
	lookup tables for common situations
	approximate evaluation(estimate value of non-terminal nodes) *deep enough*
	