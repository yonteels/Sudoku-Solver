import java.util.*;

public class valid_Sudoku {

    public static void main(String[] args) {
        String[][] board = {{"8","3",".",".","7",".",".",".","."}
        ,{"6",".",".","1","9","5",".",".","."}
        ,{".","9","8",".",".",".",".","6","."}
        ,{"8",".",".",".","6",".",".",".","3"}
        ,{"4",".",".","8",".","3",".",".","1"}
        ,{"7",".",".",".","2",".",".",".","6"}
        ,{".","6",".",".",".",".","2","8","."}
        ,{".",".",".","4","1","9",".",".","5"}
        ,{".",".",".",".","8",".",".","7","9"}};
        
        System.out.println(hello(board));
    }

    public static boolean hello(String[][] board) {
        HashSet<String> set = new HashSet<String>();

        // check horizontal row
        for (int i = 0; i < 9; i++) {
            for (int j=0; j<9;j++){
                if (set.contains(board[i][j]) && (board[i][j] != ".")) {
                    System.out.println("error"+ board[i][j]);
                    return false;
                }
                set.add(board[i][j]);
            }
            set.clear();
        }


        // check vertical row
        for (int i =0 ; i < 9; i++){
            for (int j=0; j<9;j++){
                if (set.contains(board[j][i]) && (board[j][i] != ".")) {
                    System.out.println("error at X=" +j + "Y = " +i );
                    return false;
                }
                set.add(board[j][i]);
            }
            set.clear();
        }

        // check 3x3 grid 

        int x_OS = 0; // x offset
        int y_OS =0; // y offset
         
        for (int i =0; i <9; i++){
            for (int j =0; j <3; j++){
                for (int k=0; k<3; k++){
                    if (set.contains(board[j+x_OS][k+y_OS]) && (board[j+x_OS][k+y_OS] != ".")) {
                        return false;
                    }
                    set.add(board[j+x_OS][k+y_OS]);
                }
            }
            set.clear();
            x_OS +=3;
            if (x_OS >6){
                x_OS = 0;
                y_OS +=3;
            }
        }

        return true;
    }

}
