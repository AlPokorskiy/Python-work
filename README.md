# TicTacToe-python_prj
Python Project -> Tic Tac Toe game
------------------------------------------------------------------------------------
This version is mainly for Jupiter notebook demostrations
Current method line-up for this project:
  
	-draw_board(board) 
		-> Draws the board  that the game is displayed on
  
	-position_pick() 
		-> method will ask what the user to pick either the X or O symbol to play as
  
	-draw_on_board(board, pinput, position) 
		-> receives board data, position of the marker data, and what symbol is currently inrotation (x or o)
  
	-win_checker(board, marker)
	 -> checks for the possible win conditions horizontal(3 options), vertical(3 options), or diagonal win(2 options)
  
	-chose_first() 
    -> this is a simple random  number generator between  1 and 2 to see who goes first
  
	-is_space_empty(board, position) 
    -> checks to make sure that the space is empty before continuing to the draw_on_board method
  
	-full_board(board) 
    -> checks if the board is filled up with symbols and concludes draw if that is the case
  
	-player_choice(board,player_dict) 
    -> simply prompts the player to  pick a position
  
	-play_again() 
    -> asks if the player wants to play again after a win/loss or draw
  
	-*execution cell* 
		->here the methods all get executed under certain conditions
     -creates a new 'board' list to use [' ']*10 
     -sets game_on variable to true -> this variable controls if the game look is running or now
     -curr_player = '' -> means no player data is in selection
     -sign_pick ={1:0,2:0} dictionary that holds key/value pair of player data that will be given through the chose_first() method
     -while loop (game_on)
     -executes the draw_board(game_board) method
     -executes pick_sign = position_pick()
        -if/else sets the player picks in the sign_pick dictionary 
     -go_first = chose_first() -> whatever the random number is equates to who goes first
     -curr_player = sign_pick[go_first] -> this will set the first player to go
     -while not full_board(game_board) -> this loop constantly checks to make sure the game board is not full
     -choice= player_choice(game_board,curr_player) -> retrieves the symbol the first player(player 1) picked
     -if curr_player == sign_pick[1]
          ->if player 1 goes first then run the win_checker() method 
          ->switch the other player
          ->print that the  next player is now selected
          -else announce the winner and break the loop
      -if curr_player == sign_pick[2]
          ->if player 1 goes first then run the win_checker() method 
          ->switch the other player
          ->print that the  next player is now selected
          -else announce the winner and break the loop
      -after the breaking the loop prompt the user if they wanna player again
        -if not then break and end the game
      
    
