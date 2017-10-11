# CommentsExampleProgram
/*
*
Comments Example Program
Joyce Yang
October 10, 2017
*/
import java.util.Random;
import java.util.Scanner;
public class Main
{
    public static void main(String[] args)
    {
        Scanner scan = new Scanner(System.in);
        
        //Pick random number
        Random random = new Random();
        long from = 1;
        long to = 100;
        int randomNumber = random.nextInt(to - from + 1) + from;
        //Set guess to 0
        int guessedNumber = 0;
 
        //Beginning and end of range
        System.out.printf("The number is between %d and %d.\n", from, to);
        
        //Take the user's submissions
        do
        {
            System.out.print("Guess what the number is: ");
            guessedNumber = scan.nextInt();
            if (guessedNumber > randomNumber)
                System.out.println("Your guess is too high!");
            else if (guessedNumber < randomNumber)
                System.out.println("Your guess is too low!");
            else
                System.out.println("You got it!");
        } while (guessedNumber != randomNumber);
    }
} 
