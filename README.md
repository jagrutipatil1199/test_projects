# test_projects 
package Tic_tac_game;

public class Board { 
	char [][] board; 
	public Board () 
	{ 
		board = new char[3][3]; 
		initBoard();
	} 
	void initBoard() 
	{ 
		for (int i = 0; i < board.length; i++)  
		{ 
			for (int j = 0; j < board[i].length; j++) 
			{
				board[i][j]= ' '; 
				}
			
		}
	}
 
	void dispBoard() 
	{  
		System.out.println("-------------");
		for (int i = 0; i < board.length; i++)  
		{  
			for (int j = 0; j < board[i].length; j++) 
			{
				System.out.print(board[i][j] + " | "); 
				
			} 
			System.out.println();  
			System.out.println("-------------"); 
			
		} 
	}  
	void placemark(int row, int col, char mark) 
	{ 
		if (row >=0 && row<=2 && col >=0 && col <=2); 
		{
			board[row][col] = mark; 
		}
		
			
		
	}  
	boolean checkcolwin() 
		{ 
		for(int j=0; j<=2; j++) 
		{ 
			if(board[0][j] == board[1][j] && board[1][j] == board[2][j]) 
			{ 
				return true; 
				
			} 
		} 
		return false; 
		
		}
		
	
	 
	

	
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub 
		Board  t = new Board();  
		t.dispBoard(); 
		
		t.placemark(0, 0, 'x');  
		t.placemark(0, 1, '0'); 
		t.placemark(2, 2, 'x'); 
		t.placemark(1, 1, '0'); 
		t.placemark(0, 2, 'x');  
		t.placemark(2, 1, '0');  
		 
		t.dispBoard(); 
		System.out.println(t.checkcolwin());
	} 
	} 
