=====================
Tournament Results
=====================
Tournament Results is a simple Python app that uses PostgreSQL database to store player and matches data. 
It also includes functionality to rank the players acording to their standings and pair them up in matches in a tournament.


Quick start
-----------

1. Database and table definitions are stored in the tournament.sql file.
2. The following Python functions are stored in tournament.py file:
	
	registerPlayer(name) - adds a player to the tournament by putting an entry in the database. The database should assign an ID number to the player. Different players may have the same names but will receive different ID numbers,

	countPlayers() - returns the number of currently registered players. This function should not use the Python len() function; it should have the database count the players,

	deletePlayers() - clear out all the player records from the database,

	reportMatch(winner, loser) - Stores the outcome of a single match between two players in the database,

	deleteMatches() - clear out all the match records from the database,

	playerStandings() - returns a list of (id, name, wins, matches) for each player, sorted by the number of wins each player has,

	swissPairings() - given the existing set of registered players and the matches they have played, generates and returns a list of pairings according to the Swiss system. Each pairing is a tuple (id1, name1, id2, name2), giving the ID and name of the paired players. For instance, if there are eight registered players, this function should return four pairings. This function should use playerStandings to find the ranking of players.

3. Run test suite included in the tournament_test.py file in order to test functions in the tournament.py.