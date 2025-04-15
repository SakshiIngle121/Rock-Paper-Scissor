package com.company;
import java.util.Scanner;
import java.util.Random;
public class Sak_RockPaperScissor {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("It's Your Turn \n Please Choose Your Choice :");
        Random ran = new Random();
        int i = 1;
        while(i <= 4)
        {
            int Your_Turn, Computer_Turn;
            Your_Turn = sc.nextInt(3);
            Computer_Turn = ran.nextInt(3);
            System.out.println("You Choose : ");
            switch(Your_Turn)
            {
                case 0 -> System.out.println("Rock");
                case 1 -> System.out.println("Paper");
                case 2 -> System.out.println("Scissor");
            }
            System.out.println("Computer chose : ");
            if (Computer_Turn == 0 )
            {
                System.out.println("Rock");
            }
            else if (Computer_Turn == 1)
            {
                System.out.println("Paper");
            }
            else if (Computer_Turn == 2)
            {
                System.out.println("Scissor");
            }
            System.out.println("Here is The Winner :");
            if (Your_Turn == 0 && Computer_Turn == 1)
            {
                System.out.println("Oops! The Computer won. Better Luck Next Time.");
            } else if (Your_Turn == 1 && Computer_Turn == 2)
            {
                System.out.println("Oops! The Computer won. Better Luck Next Time.");
            }
            else if (Your_Turn == 2 && Computer_Turn == 0)
            {
                System.out.println("Oops! The Computer won. Better Luck Next Time.");
            }
            else if (Your_Turn == 1 && Computer_Turn == 0)
            {
                System.out.println("Congratulations! You Won! ");
            }
            else if (Your_Turn == 2 && Computer_Turn == 1)
            {
                System.out.println("Congratulations! You Won! ");
            }
            else if (Your_Turn == 0 && Computer_Turn == 2)
            {
                System.out.println("Congratulations! You Won! ");
            }
            else if (Your_Turn == 0 && Computer_Turn == 0 || Your_Turn == 1 && Computer_Turn == 1 || Your_Turn == 2 && Computer_Turn == 2)
            {
                System.out.println(" Sorry, The Match Is Drawn. Please Play Again");
            }
        }
    }
}
