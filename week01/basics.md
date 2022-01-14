# DSA Training Questionnaire

## Week 1: Basics of Programming

1.  Make a basic calculator which inputs two numbers and an operator and outputs the desired result. Implement addition, subtraction, multiplication, division, and modulo operation

    -   Example Output
        ```
        Return first number :10
        Enter Operator: +
        Enter Second Number: 100
        10 + 100 = 110
        ```
    -   Try to also add a prompt if the operator is not supported
        ```
        Return first number :1
        Enter Operator: a
        Wrong Operator, Try Again!!
        Enter Operator: b
        Wrong Operator, Try Again!!
        Enter Operator: -
        Enter Second Number: 2
        1 - 2 = -1
        ```
    -   Try to implement power and factorial without using inbuilt functions. Make a different function for power and factorial and use them in the calculator

2.  Input a number n. Print integers 1 to N, but print “Fizz” if an integer is divisible by 3, “Buzz” if an integer is divisible by 5, and “FizzBuzz” if an integer is divisible by both 3 and 5.

    -   Example Output
        ```
        Enter a number: 10
        1
        2
        Fizz
        4
        Buzz
        Fizz
        7
        8
        Fizz
        Buzz
        ```

3.  Make a number guessing game, generate a random number [(might help)](<https://www.journaldev.com/43739/random-number-generator-c-plus-plus#:~:text=Generate%20random%20numbers%20within%20a%20range&text=For%20instance%2C%20in%20order%20to,%2B%20(%20rand%20()%20%25%209)%3B>) between 1 and 1000 and ask player to guess a number, if the player guesses correctly, display a congratulation message and exit. If the guess is incorrect, mention if the user guessed too high or too low.

    -   Example Output
        ```
        Enter a number to guess between 1 and 1000: 1
        Entered number is Too Low !!
        Enter a number to guess between 1 and 1000: 10
        Entered number is Too High !!
        Enter a number to guess between 1 and 1000: 2
        Entered number is Too Low !!
        Enter a number to guess between 1 and 1000: 3
        Entered number is Too Low !!
        Enter a number to guess between 1 and 1000: 4
        Entered number is Too Low !!
        Enter a number to guess between 1 and 1000: 5
        Congratulation You found the answer !!
        ```
    -   Now for the fun part, you can see that randomly checking is too long, how can you complete this game in minimum number of steps.
        <details><summary>Click me for a hint</summary>

        google `binary search` (It's okay if you don't get a hang of it as we will discuss it in upcoming sessions, this is supposed to be a bit tricky so don't get sad)

        </details>

4.  Write a program that prompts the user to enter a credit card number as a long integer and Display whether that card is valid or invalid.

    -   Criteria for a number to be a credit card number

        -   A credit card number must have between 13 and 16 digits.
        -   It must start with
            -   4 for Visa cards
            -   5 for Master cards
            -   37 for American Express cards
            -   6 for Discover cards

    -   Eg: `379354508162306` is a valid credit card number
    -   Eg: `4388576018402626` is an invalid credit card number
    <details>
    <summary>Implement this problem using the following algorithm</summary>

    Here we will define a special algorithm called `Luhn Check` or `Mod 10 Check` which is used for this exact problem. You will have to implement it.

    Steps for the algorithm:

    1. Double every second digit from right to left. If doubling of a digit results in a two-digit number, add up the two digits to get a single-digit, like for 12:1+2, 18=1+8).

    2. Now add all single-digit numbers from Step 1.
       Eg: `4 + 4 + 8 + 2 + 3 + 1 + 7 + 8 = 37`.

    3. Add all digits in the odd places from right to left in the card number. Eg: `6 + 6 + 0 + 8 + 0 + 7 + 8 + 3 = 38`

    4. Sum the results from Step 2 and Step 3. Eg: `37 + 38 = 75`

    5. If the result from Step 4 is divisible by 10, the card number is valid; otherwise, it is invalid.

     </details>