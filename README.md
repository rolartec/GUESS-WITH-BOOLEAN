GUESS-WITH-BOOLEAN
==================

//	By  Reina Olarte


// 	Guessing Number using BOOLEAN

import java.util.Scanner;

import java.util.Random;

public class BooleanFinal

{
		public static void main( String[]args)
{
	//Create the Scanner to input the number
	Scanner input = new Scanner(System.in);
	//Create the Random number
	Random randomNumber = new Random();

	//Declaring the variables
	int UserNumber;
	int computerNumber;
	computerNumber = 0 + (int)(Math.random() *10);
	boolean GameWon = false;
	boolean ResultLow = false;
	boolean ResultHigh = false;
	boolean EndGame = false;
	
	System.out.println("Welcome to the Guessing game\nPlease enter a digit from 0 to 10:");
	UserNumber = input.nextInt();

	if (computerNumber == UserNumber)
	{
		GameWon = true;
	}

	else
		{
			if (computerNumber < UserNumber)
			{
				ResultHigh = true;
			}
			else
			{	
				ResultLow = true;
			}	
		}

	if(GameWon)
	{
		System.out.println("You Guessed the right number");
		System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
	}
	else if (ResultHigh)
	{
		System.out.println("You Guessed to High");
		System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
	}
	else if (ResultLow)
	{
		System.out.println("You Guessed to Low");
		System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
	}
	
		
}//End main

}//End class


Hi Reina,

if (computerNumber == UserNumber)
{    
GameWon = true;
}

Can be re-written as 
    GameWon = computerNumber == UserNumber;

Please ask me in class to explain.  Please see if you can change the statement for ResultHigh and ResultLow accordingly.
