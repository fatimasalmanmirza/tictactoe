def draw_board(board):
  print("_____________")
  for row in board:
    p = "|"
    for column in row:
      p += " " + column + " "
      p += '|'
    print(p) 
    print("_____________")
  print("")
  print("")
  print("")



def greetings():
  """print the introduction"""
  print("Welcome to tic tac toe game")
  print()
  print("Some rules of the tic tac toe game are:")
  print("1. There will be two players in this game.")
  print("2. player 1 will make the first move and player 2 will make the next.")
  print("3. player 1 move will be represented by X on the board whereas player 2 will be represented as O.")
  
  print()
  print("Excited to play this game? So lets get started!")
  print()
  print("Enter you names:")


def getting_names():
  """getting user names and aasigning it to variable"""  

  player_1 = input("what is player 1 name?")
  player_2 = input("what is player 2 name?")
  print("Hi, {} and {}".format(player_1,player_2))
  return player_1,player_2 

 
   

def check_winner(tic_tac_toe_board):
  """checking winner"""
  winner = False
    
  if tic_tac_toe_board[0][0] == tic_tac_toe_board[0][1] == tic_tac_toe_board[0][2] == "X" or tic_tac_toe_board[1][0] == tic_tac_toe_board[1][1] == tic_tac_toe_board[1][2] == "X" or tic_tac_toe_board[2][0] == tic_tac_toe_board[2][1] == tic_tac_toe_board[2][2] == "X" or tic_tac_toe_board[0][0] == tic_tac_toe_board[1][1] == tic_tac_toe_board[2][2] == "X" or tic_tac_toe_board[0][2] == tic_tac_toe_board[1][1] == tic_tac_toe_board[2][0] == "X" or tic_tac_toe_board[0][0] == tic_tac_toe_board[1][0] == tic_tac_toe_board[2][0] == "X" or tic_tac_toe_board[0][1] == tic_tac_toe_board[1][1] == tic_tac_toe_board[2][1] == "X" or tic_tac_toe_board[0][2] == tic_tac_toe_board[1][2] == tic_tac_toe_board[2][2] == "X":
     
      winner = 1
      
    
   
  elif tic_tac_toe_board[0][0] == tic_tac_toe_board[0][1] == tic_tac_toe_board[0][2] == "O" or tic_tac_toe_board[0][0] == tic_tac_toe_board[0][1] == tic_tac_toe_board[0][2] == "O" or tic_tac_toe_board[2][0] == tic_tac_toe_board[2][1] == tic_tac_toe_board[2][2] == "O" or tic_tac_toe_board[0][0] == tic_tac_toe_board[1][1] == tic_tac_toe_board[2][2] == "O" or tic_tac_toe_board[0][2] == tic_tac_toe_board[1][1] == tic_tac_toe_board[2][0] == "O" or tic_tac_toe_board[0][0] == tic_tac_toe_board[1][0] == tic_tac_toe_board[2][0] == "O" or tic_tac_toe_board[0][1] == tic_tac_toe_board[1][1] == tic_tac_toe_board[2][1] == "O" or tic_tac_toe_board[0][2] == tic_tac_toe_board[1][2] == tic_tac_toe_board[2][2] == "O":
      
      winner = 2
    
  return winner
      

 
def check_tie(tic_tac_toe_board):

	"""Checks if board is full and there's a tie"""
	tie = True
	draw_board(tic_tac_toe_board)
	for row in tic_tac_toe_board:
		for space in row:
			if space == " ":
				tie = False
				break
	return tie
    

# global variables
board_key = [
  ["00","01","02" ],
["10","11","12" ],
["20","21","22"]
]
tic_tac_toe_board = [
  [" "," "," "],
  [" "," "," "],
  [" "," "," "]
]

##game starts here
greetings()
getting_names()
draw_board(board_key)
print("make a move?") 
while True:
  
   #  player1 will write the place number
  print("player1 enter place number")
  place_of_player1 = input("> ") 
  row = int(place_of_player1[0])
  col = int(place_of_player1[1])
 # ensure place numbers are valid 
  while row > 2  or col > 2:
    print("invalid move.please try again")
    place_of_player1 = input("player1 enter place number")
  
      
 # checking tie and winner   
  tie = check_tie(tic_tac_toe_board)
  winner = check_winner(tic_tac_toe_board)
  if winner:
    print("congratulations player {} wins".format(winner)) 
    break
  if tie:
    print("it's a tie")
    break  
  #print plave number to board  
  else:
    tic_tac_toe_board[row][col] = "X"
    draw_board(tic_tac_toe_board) 
    # player2 move
  #asking player2 move
    place_of_player2 = input("player2 enter place number?")
      
    row = int(place_of_player2[0])
    col = int(place_of_player2[1])
      
    # ensure place numbers are valid 
    if row > 2 or col > 2:
      print("invalid move.please try again")
      place_of_player2 = input("player2 enetr you place number?")
    else:
      #checking tie and winner
      tic_tac_toe_board[row][col] = "O"
      winner = check_winner(tic_tac_toe_board)
      tie = check_tie(tic_tac_toe_board)
        
      if winner:
          print("congrations player {} wins".format(winner))
        
          break 
      if tie:
          print("it's a tie")
         
          break
      else:
          continue  
