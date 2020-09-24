# How to use:
	-- run the python script api.py

# Dependencies:
	Install the dependencies using following command:
	In windows:
		-- pip install -r requirements.txt
	In Linux:
		-- pip3 install -r requirements.txt


# Example:

	To start the game:
		# call the api -- "https://127.0.0.1/game/4connect/start"

		# Hitting this api first reset the board for the new game.

		# This returns the response [ "READY" ] after resetting the board.

	To make a move:
		# call the api -- "https://127.0.0.1/game/4connect/move/<player-number>/<column-number>"

			player-number varies from 1 to 2
			column-number varies from 0 to 6

		# This returns the response for the following cases:

			(1) when either of the player wins, the respose is -- [ "<Player-color> wins" ].

			(2) when the column number is invalid or the board is completely filled and no further move is possible, the 	response is -- [ "INVALID" ]

			(3) For each valid move, the response is [ "VALID" ]
