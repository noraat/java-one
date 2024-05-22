1. Diving deep into boolean
2. Introduction to statements
3. Introduction to different operators

```java
public class Main {

  static int sharedValue = 200;
  
  public static void main(String[] args) {
    System.out.println("Hello world!");
    // winter, spring, summer, autumn
    // warm jacket, t-shirt, swimming suite, rain coat 
      double temp = 2;

      if (temp <= 5) {
        String message = "The weather is good outside!";
        System.out.println(message);
      }
      else if (temp <= 15) {
        System.out.println(message);
      }
      else if (temp <= 30) {
        System.out.println(message);
      }
      else {
        System.out.println(message);
      }
  
      // class level on seal kõige ees ja scope level on see, mis iga ifi juures või nende { } vahel. 
  }

}
```



#Lesson 4, Topic: Statements ||

1. Using if/else if/else
2. Different logical puzzles with if statements
3. Introduction in scope

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
 Scanner input = new Scanner(System.in);

    System.out.println("What is your name? ");
    String name = input.nextLine();
    
    System.out.println("What is your age? ");
    int age = input.nextInt();  

    input.nextLine();
    
    System.out.println("What are your favourite vegetables? ");
    String vegetable = input.nextLine();
    
    System.out.println("What´s the temperature outside right now? ");
    float temperature = input.nextFloat();
    
    if (temperature > 15) {
        System.out.println("It's hot outside");
    } else {
        System.out.println("Bring a jacket! It's cold outside! \n");
    }

    
  System.out.println("Your name is " + name + " and your are " + age + " years old." + " For some reason you like " + vegetable + " a lot." + " The temperature outside right now is " + temperature + " degrees.");

    input.close();

  }

}


//Team work: Create a program, that asks user some questions and then creates a story based on the values.

```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    int number = 58;

    // 1. We have a number

    // 2. We ask for the user to guess the number
    // 3. If the guessed number is bigger, then we say "Too big"
    // 4. If the guessed number is smaller, then we say "Too small"
    // 5. If the guessed number is correct, then we say "Correct"
    // 2-5 line a loop, we stop the loop, when the user is correct

    while (true) {
      System.out.println("Please guess a number!");
      int guess = scanner.nextInt(); // A number that user provides

      if (number == guess) {
        System.out.println("Good job, you guessed correctly");
        break;
      } 
      if (number < guess) {
        System.out.println("Sorry, the number is too big");
        continue;
      }
      System.out.println("Sorry, the number is too small");
    }
    System.out.println("Guessing game is over!");
    scanner.close();
  }
}
```



```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of lines for the triangle: ");
        int lines = scanner.nextInt();
        for (int i = 1; i <= lines; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("_");
            }
            System.out.println(); // Move to the next line after printing each line
        }
        scanner.close();
    }
}
```

```java

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Welcome to the Number Guessing Game!");
        System.out.println("The programmer has picked a number between 0 and 100 (inclusive).");

        // Generate a random number between 0 and 100 (inclusive)
        int chosenNumber = 55;

        int guess; // Variable to store the player's guess

        // Loop until the correct number is guessed
        while (true) {
            // Prompt the player to make a guess
            System.out.println("Make a guess: ");
            guess = input.nextInt();

            if (guess == chosenNumber) {
                System.out.println("Congratulations! You guessed the correct number: " + chosenNumber);
                break; // Exit the loop
            } else if (guess < chosenNumber) {
                System.out.println("The number is bigger than " + guess + ". Try again.");
            } else {
                System.out.println("The number is smaller than " + guess + ". Try again.");
            }
        }

        input.close(); // Close the Scanner object
    }
}
```


```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in); // opening a channel for user input
    System.out.println("Please write a number! ");
    int number = scanner.nextInt(); // waiting for a number from user

    String result = ""; // an empty string
    
    for(int i = 1; i <= number; i++) {  
      // for(int i = 1; runs before the cycle, 
      //i <= number - then we condition i to the number person wrote. if it is smaller or equal, then we go in the fist cycle of the loop - 
      // i++ is what we do at the end of the cycle i++ means i = i + 1
      
      result = result + "_";
      System.out.println(result);
    }

    scanner.close();
  }
}


// 1. get user input - x
// 2. Create a loop that runs x amount of times
// 3. Inside the loop, print _ symbol i times
```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner scanner = new Scanner(System.in);
    int number = 58;

    //1. We have a number

    //2. We ask for the user to guess the number
    //3. If the guessed number is bigger, then we say  "Too big"
    //4. If the guessed number is smaller, then we say "Too small"
    //5. If the guessed number is correct, then we say "Correct"
    //2-5 line a loop, we stop the loop, when the user is correct
    boolean userGuessedCorrectly = false;
    while(!userGuessedCorrectly) {
      System.out.println("Please guess a number!");
      int guess = scanner.nextInt(); //A number that user provides

      if(number == guess) {
        System.out.println("Good job, you guessed correctly");
        userGuessedCorrectly = true;
      }
    }
    System.out.println("Guessing game is over!");
    scanner.close();
  }
}
```


#ARRAYS

```java
public class Main {
  public static void main(String[] args) {
    int[] arr = new int[5];
    arr[0] = 5;
    arr[1] = 7;
    arr[2] = 9;
    arr[3] = 12;
    arr[4] = 15;


    for(int i = 0; i < arr.length; i++){
      System.out.println(arr[i]);
    }

  }

```

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter 5 city names: ");

        String[] arr = new String[5];
        for (int i = 0; i < arr.length; i++)
            arr[i] = scanner.nextLine();

        System.out.println("You entered: ");
        for (int i = 0; i < arr.length; i++)
            System.out.println(arr[i]);
    }
}



//Easy -> Initialize a string array and try to input and output data
//We want to define an array city names.
//We want to add values to it (could be through the scanner, or just writing 

//arr[0] = "Riga";


//With scanner
//arr[0] = scanner.nextLine();

//Challenging -> Find the largest number in the array and find the smallest number in the array
```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    System.out.println("Please enter 5 numbers from 0-100: ");

    int[] arr = new int[5];
    for (int i = 0; i < 5; i++)
      arr[i] = scanner.nextInt();
    
    System.out.println("You entered: ");
    for (int i = 0; i < 5; i++)
      System.out.println(arr[i]);

    int maxNumber = arr[0];
    for (int i = 0; i < 5; i++)
      if (arr[i] > maxNumber)
        maxNumber = arr[i];
    System.out.println("Max number is: " + maxNumber);

    int minNumber = arr[0];
    for (int i =0; i < 5; i++)
      if (arr[i] < minNumber)
        minNumber = arr[i];
    System.out.println("Min number is: " + minNumber);
  }
}
```



```java
/*

We have an array with different numbers {1, 3, 4, 2, 5, 8}

User is providing a number

Check whether or not this number exists in the array
*/

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    int[] numbers = { 1, 3, 4, 2, 5, 8 }; // numbers.length = size of the numbers = 6

    System.out.println("Please write your favourite digit");

    Scanner scanner = new Scanner(System.in);
    int favouriteNumber = scanner.nextInt();

    boolean isFound = false;

    for (int i = 0; i < numbers.length; i++) {

      if (numbers[i] == favouriteNumber) {
        isFound = true;
        break; //EXITS THE FOR LOOP ALTOGETHER, ignoring the i < numbers.length
      }

    }
    if(isFound){
      System.out.println("Your favourite number " + favouriteNumber + " is in the array");
    } else {
      System.out.println("Your favourite number " + favouriteNumber + " is NOT FOUND!");
    }

    scanner.close();
  }
}
```


```java
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Random rand = new Random();
        int[] randomNumbers = new int[5];
        int sum = 0;

        System.out.println("Randomly generated numbers: ");

        for (int i = 0; i < randomNumbers.length; i++) {
            randomNumbers[i] = rand.nextInt(101) - 50; // Random numbers between -50 and 50
            System.out.println(randomNumbers[i]);
            sum += randomNumbers[i];
        }

        System.out.println("Negative numbers:");

        for (int i = 0; i < randomNumbers.length; i++) {
          if(randomNumbers[i] < 0) {
                System.out.println(randomNumbers[i]);
            }
        }

        System.out.println("The sum of all numbers: " + sum);

        kala(); // Call the kala function

    }

    public static void kala() {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter a name you want to check: ");
        String checkPerson = scanner.next();

        String [] names = {"Anna", "Oskars", "Maris"};
        boolean found = false;

        for (String person : names) {
            if (person.equals(checkPerson)) {
                found = true;
                break;
            }
        }

        if (found) {
            System.out.println("The name " + checkPerson + " is on the list");
        } else {
            System.out.println("Not in the list");
        }
    }
}

```



```java
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Random rand = new Random();
        int[] randomNumbers = new int[5];
        int sum = 0;

        System.out.println("Randomly generated numbers: ");

        for (int i = 0; i < randomNumbers.length; i++) {
            randomNumbers[i] = rand.nextInt(101) - 50; // Random numbers between -50 and 50
            System.out.println(randomNumbers[i]);
            sum += randomNumbers[i];
        }

        System.out.println("Negative numbers:");

        for (int i = 0; i < randomNumbers.length; i++) {
          if(randomNumbers[i] < 0) {
                System.out.println(randomNumbers[i]);
            }
        }

        System.out.println("The sum of all numbers: " + sum);

        kala(); // Call the kala function

    }

    public static void kala() {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter a name you want to check: ");
        String checkPerson = scanner.next();

        String [] names = {"Anna", "Oskars", "Maris"};
        boolean found = false;

        for (String person : names) {
            if (person.equals(checkPerson)) {
                found = true;
                break;
            }
        }

        if (found) {
            System.out.println("The name " + checkPerson + " is on the list");
        } else {
            System.out.println("Not in the list");
        }
    }
}

```


```java
public class Main {
  public static void main(String[] args) {
    printOutABorder();
    printOutABorder();
    int number = getARandomNumber();
    System.out.println(number);
    printOutABorder();
    
  }

  public static void printOutABorder() {
    System.out.println("===========");
  }

  
   public static int getARandomNumber() {
      return 5;
  }
  
}
```


```java
public class Main {
  public static void main(String[] args) {
    int number1 =5;
    int number2 =7;
    int result = sum(number1, number2)
      System.out.println(result);
   
  }


  public static int sum (int number1, int number 2) {
    return number1 + number2;
  }
}
```


```java
/*
  Write a name and check whether or not it is atleast 3 char long
   Write a surname and check whether or not it is atleast 3 char long
If it's not, then say. Sorry, your name is too short.
If both of them are valid, say. Thank you, your information has been registered!
*/

public class Main{
  public static void main(String[] args){

    String name = "Oskars";
    String surname = "Klaumanis";
    boolean isUserNameValid = isNameValid(name);
    boolean isUserSurnameValid = isNameValid(surname);

    if(isUserNameValid && isUserSurnameValid){
      System.out.println("Thank you, your information has been registered!");
    } else {
      System.out.println("Sorry, your check your information");
    }

  }

  public static boolean isNameValid(String name){
    if(name.length() < 3){
      System.out.println("Sorry, your name is too short.");
      return false;
    }

    return true;
  }
}
```


```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
  Scanner scanner = new Scanner(System.in);
    System.out.println("Enter number 1: ");
    int number1 = scanner.nextInt();
    
    System.out.println("Enter number 2: ");
    int number2 = scanner.nextInt();

    int result = sum(number1, number2);
      System.out.println(result);
    
  }

  public static int sum (int number1, int number2) {
    return number1 + number2;
  }
}



/*

Easy:

Sum of 2 numbers
User provides 2 numbers
Result is a sum of those numbers

Example: 
User inputs 5
User inputs 6
Result: 11

Hard:
1. Create a program, where user can provide a title and a small text below the title.
Title should be wrapped with ====== at top and bottom, based on the title length.
Example: 
System asks for title and user provides "WoTech and Java is easy"
System asks for description and user provides "I have been learning Java for 6 weeks now."

Result: 
=======================
WoTech and Java is easy
=======================

I have been learning Java for 6 weeks now.

*/
```

```java
public class Main {
  public static void main(String[] args) {
    int number = 51;

    checkNumber(number);

    int number2 = 49;

   checkNumber(number2);
    
    /* We get the number
    We check whether or not it is bigger than 50
    We check whether or not it is smaller than 50
    We assume it is equal to 50 if all of the upper conditions are false
    */
  }

  // void is just for action
  // int it is for returning a number
  // String is returning a text
  // boolean is for returning a true or false

  
  public static void checkNumber(int value){
    if(value > 50){
      System.out.println("Number is greater than 50");
    }else if(value < 50){
      System.out.println("Number is less than 50");
    }else{
      System.out.println("Number is equal to 50");  
    }
  }
}
```


```java
public class Main {
  public static void main(String[] args) {
    int money = 50;
  

    String result = buyJeans(money);

    System.out.println(result);

    
  }

  public static String buyJeans(int value){
    int price = 30;
    int price2 = 20;
    if(value > price + price2)
    {
      return "You can buy jeans";
    }else{
      return "You can't buy jeans";
    }

    
  }

  
}
```


```java
// 7, 12, 18 
// Needs to sum them all together


public class Main {
  public static void main(String[] args) {
    int number1 = 7;
    int number2 = 12;

    int number3 = 18;

    int result = sum(number1, number2); // 7 + 12 = 19

    int finalResult = sum(result, number3); // 19 + 18 = 37

    System.out.println(finalResult);
  }

  public static int sum(int a, int b){
    return a + b;
  }
}
```

```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {

    Scanner inputNumber = new Scanner(System.in);
    System.out.print("Enter the first number: ");
    int number1 = getNumber();

    System.out.print("Enter the second number: ");
    int number2 = getNumber();

    getSmallest(number1, number2);

  }

   public static int getNumber(){
     Scanner scanner = new Scanner(System.in);
     int number = scanner.nextInt();

     return number;
  
  
   }

  public static void getSmallest(int number1, int number2) {
    if (number1 < number2) {
      System.out.println(number1 + " is the smallest number");
    } else {
      System.out.println(number2 + " is the smallest number");
    }
    

    }
}  

/*

Easy:
1. Create a function that returns smallest number of 2 numbers.

For example:
User provides 5
User provides 7

Function returns 5
Main function prints out:
5 is the smallest number

2. Create a function that returns a multiplication of 3 different numbers
For example: 
User provides 5
User provides 7
User provides 3

Function returns 105
Main function prints out 105


medium:
1. Parent simulator, a user provides a number (average grade) to the program, and if it's above 8, then parents go hooray, else they go sad

User creates 3 functions
    1. Function called hooraay(), is a void, and returns nothing. It's only job is to print out "Hooraay" in the console
    2. Function called sad(), is a void, and returns nothing. It's only job is to print out "Sad" in the console
    2. Function is called CheckGrades and receives int as value, but returns nothing. It's job is to call hooray() function, if the grade that it received is above 8, and call sad() function, if the grades received is less than 8



3. Create a function that returns a combination of first name and last name
User provides "Oskars"
User provides "Klaumanis"

Function receives both of the names and returns "Oskars Klaumanis"
Main function prints out the result


Hard:
1. Fill the party list with people you would like to invite to the party.
Check whether or not "Anna" is in the array.
Check whether or not "Maris" is in the array.
["Oskars", "Anna", "Andris"]
Result: 
"Anna is in the party list"
"Maris is not in the party list"



2. Guess the Number Game
Generate a random number from 0 to 100
Make the user guess the number. If it's too high, or too low, let the user know
OPTIONAL: Give maximum of 6 guessues.


Very hard:
1. Grades in university
You have 3 students, each one of them has grades. (three different int arrays) 
Calculate the average grade for each student (sum of all grades and divide by grade count)

Example:
robertsGrades {8, 6, 7, 9, 10}
annasGrades {7, 10, 10, 9, 6}
franceskasGrades {8, 8, 8, 7, 6}

Result:
Robert's average grade is 8
Anna's average grade is 8.4
Franceska's average grade is 7.4

*/
```

```java
import java.util.Scanner;

/*
  Ask user for a title - inputText()
  Ask user for a description - inputText()


  PrintInformation()
    Figure out the size of title
    Print out a border of the size of the title -> printBorder()
    Print out the title
    Print out a border of the size of the title -> printBorder()
    Print out the description
*/


public class Main {
  public static void main(String[] args) {

    //Creating scanner
    Scanner scanner = new Scanner(System.in);

    //Calling method for getting title
    System.out.print("Enter a title: ");
    String title = getText();

    System.out.print("Enter a description: ");
    String description = getText();

    //Calling method to get printout with lines
    getPrintout(title, description);

    //Closing scanner
    scanner.close();
  }

  // Method to ask user for description
  public static String getText() {
    Scanner scanner = new Scanner(System.in);

    //Read user input
    String text = scanner.nextLine();

    //Return user input
    return text;
  }

    // Method to display the result with the title wrapped in = characters + description

  public static void getPrintout(String title, String description) {

    // Calc length
    int length = title.length();
    // Create top border
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");
    // Display the title
    System.out.print(title);

    System.out.println("");
    // Create bottom border
    for (int i = 0; i < (length); i++) {
      System.out.print("=");
    }
    System.out.println("");

    // Display the description
    System.out.println("");
    System.out.println(description);

  }
}
```


```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    scanner inputNum = new Scanner(System.in);
    System.out.println("Enter number 1: ");
    

    
  }
  
  public static int getNumber(){
     Scanner scanner = new Scanner(System.in);
     int number = scanner.nextInt();

     return number;

  
}




/* 

2. Create a function that returns a multiplication of 3 different numbers
For example: 
User provides 5
User provides 7
User provides 3

Function returns 105
Main function prints out 105 

*/
```

```java
import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Scanner human = new Scanner(System.in);
        System.out.println("Please enter 1 for rock, 2 for scissors, 3 for paper: ");
        int humanChoice = human.nextInt();
        System.out.println("You chose: " + humanChoice);

        Random random = new Random();
        int computerChoice = random.nextInt(3) + 1;
        System.out.println("The computer randomly chose: " + computerChoice);

        

        mathTime(humanChoice, computerChoice);
    }

    public static void mathTime(int humanChoice, int computerChoice) {
        if (humanChoice == computerChoice) {
            System.out.println("You tied!");
        } else if ((humanChoice == 1 && computerChoice == 2) ||
                   (humanChoice == 2 && computerChoice == 3) ||
                   (humanChoice == 3 && computerChoice == 1)) {
            System.out.println("You won!");
        } else {
            System.out.println("You lost!");
        }
    }

}

  /* public static void winCon(int number1, int number2) {
    if (number1 < number2) {
      System.out.println(number1 + " is the smallest number");
    } else {
      System.out.println(number2 + " is the smallest number");
    }


    }

  

  

}

/*

Teamwork: Decompose a simple rock paper scissor game. Think of how many different conditions / combinations are in the game. Write down a winning conditions. Write down losing conditions.


kivi vs paber 1 vs 3
kivi vs käärid 1 vs 2
kivi vs kivi 1 vs 1 

paber vs käärid
paber vs paber

käärid vs käärid 

*/
```


```java
import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int humanChoice = getHumanChoice(scanner);
        int computerChoice = generateComputerChoice(random);

        System.out.println("You chose: " + humanChoice);
        System.out.println("Computer chose: " + computerChoice);

        determineWinner(humanChoice, computerChoice);

        scanner.close();
    }

  private static int getHumanChoice(Scanner scanner) {
      System.out.println("Please enter: \n 1 for rock \n 2 for scissors \n 3 for paper \n");
      int choice = scanner.nextInt();

      if (choice < 1 || choice > 3) {
          System.out.println("Invalid input. Please enter 1, 2 or 3.");
         
          return getHumanChoice(scanner);
      }

      return choice;
  }

    private static int generateComputerChoice(Random random) {
        return random.nextInt(3) + 1;
    }

    private static void determineWinner(int humanChoice, int computerChoice) {
        if (humanChoice == computerChoice) {
            System.out.println("You tied!");
        } else if ((humanChoice == 1 && computerChoice == 2) ||
                   (humanChoice == 2 && computerChoice == 3) ||
                   (humanChoice == 3 && computerChoice == 1)) {
            System.out.println("You won!");
        } else {
            System.out.println("You lost!");
        }
    }
}
```


```java

public class Main {
    public static void main(String[] args) {
        int[] arr = {8, 7, 5, 3, 2, 1}; // current race results
        int number = 0; // our result
        boolean thePlaceIsFound = false;
        forrepl(int i = 0; i < arr.length; i++){
            if(arr[i] < number){
                i = i + 1;
                System.out.println("Our place in race: " + i);
                thePlaceIsFound = true;
                break;
            }
        }

        if(thePlaceIsFound == false){
            System.out.println("Our place in race: " + (arr.length + 1));
        }
    }
}

/* 
1. Go through the array - for loop
2. Find a number less than our number - if
    3. Increment index by 1 
    4. Return index
5. If we cant find the number that is less than our number
    6. Return total count + 1
  */
```

```java

public class Main {
    public static void main(String[] args) {
        int[] arr = {8, 7, 5, 3, 2, 1}; // current race results
        int number = 4; // our result
        int place = getThePlace(arr, number);
        System.out.println("Our place in race: " + place);
    }

    public static int getThePlace(int[] arr, int number){
        for(int i = 0; i < arr.length; i++){
            if(arr[i] < number){
                return i + 1;
            }
        }
        return arr.length + 1;
    }
}

```


```java

/*

1. Go through the numbers from 2 to (number - 1) 

2. check whether or not it is dividable (number % i == 0)

3. If the 2nd point is true then its a prime number

4. If the 2nd point is false then it is not a prime number

*/
public class Main {
    public static void main(String[] args) {
        for(int i = 0; i < 100; i++){
            boolean isAPrimeNumber = isPrime(i);
            System.out.println(i + " is a prime number - " + isAPrimeNumber);
        }
    }

    public static boolean isPrime(int number){
        for(int i = 2; i < number; i++){
            if(number % i == 0){
                return false;
            }
        }
        return true;
    }
}
```


```java
public class Main {
    public static void main(String[] args) {
        int[][] array = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for(int i = 0; i < array.length; i++){ 
            //array[0] = {1, 2, 3}
            //array[0].length = 3
            int[] row = array[i]; // {1, 2, 3} OR {4, 5, 6} OR, {7, 8, 9}
            for(int j = 0; j < row.length; j++){ //PROCESSING ROWS HERE
                System.out.print(row[j]); 
            }
            System.out.println();


        }  
    }
}
```


```java

public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];
        int counter = 1;

        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                array[i][j] = counter++;
            }
        }

        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                if(array[i][j] < 10){
                    System.out.print(array[i][j] + "  ");
                }
                else{
                    System.out.print(array[i][j] + " ");
                }
            }
            System.out.println();
        }
    }
}



// Fill the 5x5 array with numbers from 1 to 25
// 1 2 3 4 5
// 6 7 8 9 10
// ...
// But you have to use for loop to fill it up automatically.
```

```java

import java.util.Random;

public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];
        Random random = new Random();

        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                array[i][j] = random.nextInt(9) + 1;
            }
        }

        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                if(array[i][j] < 10){
                    System.out.print(array[i][j] + "  ");
                }
                else{
                    System.out.print(array[i][j] + " ");
                }
            }
            System.out.println();
        }
    }
}
```



```java
public class Main {
    public static void main(String[] args) {
        int[][] array = new int[5][5];
        int counter = 1;

        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                array[i][j] = counter++;
            }
        }

        for(int i = 0; i < array.length; i++){
            for(int j = 0; j < array[i].length; j++){
                if(array[i][j] < 10){
                    System.out.print(array[i][j] + "  ");
                }
                else{
                    System.out.print(array[i][j] + " ");
                }
            }
            System.out.println();
        }
    }
}



// Fill the 5x5 array with numbers from 1 to 25
// 1 2 3 4 5
// 6 7 8 9 10
// ...
// But you have to use for loop to fill it up automatically.
```


```java

public class Main {
  public static void main(String[] args) {
    int number = 20;
    number = changeNumber(number);
    System.out.println(number);
    int numberVoid = 20;
    changeNumberVoid(numberVoid);
    System.out.println(numberVoid);
  }

  public static int changeNumber(int number){
    number = 55;
    return number;
  }

  public static void changeNumberVoid(int number){
    number = 55;
  }
}
```

```java
public class Main {
    public static void main(String[] args) { // Main method
        int[] array = { 1, 2, 3, 4, 5 }; // 1. declare an array
        array = changeArray(array); // 2. change the content of the array
        printOutArray(array); // 3. print out the values of the array

        int[] arrayVoid = { 1, 2, 3, 4, 5 }; // 4
        changeArrayVoid(arrayVoid); // 5
        printOutArray(arrayVoid); //6
    }

    public static int[] changeArray(int[] array) { // 2
        for (int i = 0; i < array.length; i++) { // 2.1.
            array[i] = 0; // 2.2
        } // 2.3
        return array; // 2.4
    }

    public static void changeArrayVoid(int[] array) { //5
        for (int i = 0; i < array.length; i++) { // 5.1
            array[i] = 1; // 5.2
        }// 5.3
    }

    public static void printOutArray(int[] array) { // 3 // 6
        for (int i = 0; i < array.length; i++) { // 3.1 //6.1
            System.out.println(array[i]);// 3.2 // 6.2
        } // 3.3 // 6.3
    }
}
```


```java
public class Main {
    public static void main(String[] args) { // Main method
        int size = 10;
        int[][] grid = new int[size][size];
        int bombColumn = 1;
        int bombRow = 1;
        // 1 1 1 0 0 0 0 0 0 0
        // 1 5 1 0 0 0 0 0 0 0
        // 1 1 1 0 0 0 0 0 0 0
        // 0 0 0 0 0 0 0 0 0 0
        // .... times 10

      grid[bombRow][bombColumn] = 5; // Center
      grid[bombRow - 1][bombColumn] = 1; // Top middle
      grid[bombRow - 1][bombColumn - 1] = 1; // top left
      grid[bombRow - 1][bombColumn + 1] = 1; // top right

      grid[bombRow + 1][bombColumn] = 1; // bottom middle
      grid[bombRow + 1][bombColumn - 1] = 1; //bottom left
      grid[bombRow + 1][bombColumn + 1] = 1; //bottom right

      grid[bombRow][bombColumn - 1] = 1; // middle left
      grid[bombRow][bombColumn + 1] = 1; //middle right



        printArray(grid, size);
    }

    public static void printArray(int[][] array, int size) {
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                System.out.print(array[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```


```java

//this is the main piece of the program (Public class Main)

public class Main {
  public static void main(String[] args) {

    //This is a string
    var text = "This is a random text";
    text = "this is another text";
    text = "March";
    //viimane rida on see, mis overridib eelmise

    //boolean
    var isDisabled = false;
    isDisabled = true;

    //boolean võib olla ka vari asemel
    boolean gameOver = false;
    gameOver = true;

    boolean clientIsActive = true;
    clientIsActive = false; 
    // see true ja false tähendab, et kunagi võib olla true ja kunagi võib olla false

    //number
    var number = 5;
    number = number + 7;

    text = text + " " + number; 

    //float, character
    var interestingNumber = 1.5;

    var mixedInterestingNumber =
interestingNumber + number; 

    var newCoolNumber = mixedInterestingNumber + (number * number);

    // kui kasutada \n siis tuleb uus rida 
    // \t on tab ehk siis hakkab veidi kaugemalt pihta 
    //string on alati " " sees ja sa nimetad seda stringiks
    
    String name = "Liisa";
    String surname = "Karjalainen";
    int age = 25;
    String country = "Estonia";
    var yearBorn = 2024 - (age);
    String gender = "female";
    String hairColour = "red";
    String eyeColour = "brown";
    String pet = "hamster";
    var hasChildren = true;
    hasChildren = false; 

    String bankName = "Bank of Ducks";
    bankName = bankName.toUpperCase();
    var liisaAccountNumber = "123456";
    int liisaMoneyOnAccount = 1000;
    int liisaSavings = 200;
    int liisaTotalMoney = liisaMoneyOnAccount + liisaSavings;
    int liisaPetBills = 300;
    int liisaTotalMoneyAfterPetBills = liisaTotalMoney - liisaPetBills;


    System.out.println(name + " " + surname + " " + "is" + " " + age + " years old." + "\n" +  "She is from" + " " + country + ".");
    


    System.out.println(name);
    System.out.println(age);
    System.out.println(gender);
    System.out.println(hairColour);
    System.out.println(eyeColour);
    System.out.println(pet);
    System.out.println(hasChildren);
    System.out.println(yearBorn + "\n");
    
    System.out.println(bankName);
    System.out.println(liisaAccountNumber);
    System.out.println(liisaMoneyOnAccount);
    System.out.println(liisaSavings);
    System.out.println(liisaTotalMoney);
    System.out.println(liisaPetBills);
    System.out.println(liisaTotalMoneyAfterPetBills);



    
    //System.out.println("Hello world!");
    //System.out.println(text);
    //System.out.println(isDisabled);
    //System.out.println(number);
    //System.out.println(interestingNumber);
    //System.out.println(mixedInterestingNumber);
    //System.out.println(newCoolNumber);
    
  }

}
```



```java
public class Main {
  public static void main(String[] args) {
    String studentName = "Anna";
    int yearOfSchool = 12;
    double studentAge = 18;
    double grade = 6.8;  
    boolean olympicsWinner = true;
    
    boolean isAgeEligible = studentAge >= 18;
    boolean isGradeEligible = grade >= 8;

    if (isAgeEligible && (isGradeEligible || olympicsWinner)) {
      System.out.println("You are accepted!");
    } else {
      System.out.println("You are not accepted. Reasons:");

      if (!isAgeEligible) {
        System.out.println("- You are not eligible due to age.");
      }
      if (!isGradeEligible && !olympicsWinner) {
        System.out.println("- You are not eligible due to insufficient grade.");
      }
      if (!olympicsWinner && isAgeEligible && isGradeEligible) {
        System.out.println("- You are not eligible due to not being an Olympics winner.");
      }
    }
  }
}

```

```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Let's go and check out what is in the fridge!");
    var isFridgeOpen = true;
    String result;
    // string result tähendab, et result on alati tekst. Me ei andnud sellele seal üleval tähendust, sest see tuleb hiljem. 

    if (isFridgeOpen) {
      var item1 = "Cheese ";
      var item2 = "Milk ";
      var item3 = "Eggs ";
      result = item1 + item2 + item3;
    } else {
      result = "Fridge is closed, open the fridge";
    }

    System.out.println(result);
    // ERROR System.out.println(item1);
  }
}

```
