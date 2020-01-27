import java.util.Random;
import java.util.Scanner;

public class GameOfNIM {
    private static Scanner playerInput = new Scanner(System.in);
    private static int sticks = 10;

    public static void main(String[] args) throws InterruptedException {
        System.out.println("Welcome to the Game of NIM!");
        playGame();
    }

    public static void playGame() {
        while(sticks != 0){
            computerTurn();
            if (sticks == 0)
                System.out.println("Computers wins!");
            else {
                System.out.println("There are " + sticks + " left.");
                playerTurn();
                if (sticks == 0)
                    System.out.println("Player wins!");
                else
                    System.out.println("There are " + sticks + " left.");
            }
        }
    }

    public static void computerTurn() {
        System.out.print("Computers turn to choose a number: ");
        boolean legalMove = false;
        while (legalMove == false){
            Random random = new Random();
            int computer = random.nextInt(4);
            if(computer > sticks || computer == 0){
                legalMove = false;
            }
            else{
                System.out.println(computer);
                legalMove = true;
                sticks = sticks - computer;
            }
        }
    }

    public static void playerTurn() {
        System.out.println("Players turn to choose a number: ");
        boolean legalMove = false;
        while (legalMove == false) {
            Scanner scanner = new Scanner(System.in);
            int input = scanner.nextInt();
            if (input > sticks || input == 0 || input > 3) {
                legalMove = false;
                System.out.println("That is an illegal move, please pick a different number.");
            }
            else {
                legalMove = true;
                sticks = sticks - input;
            }
        }
    }
}
