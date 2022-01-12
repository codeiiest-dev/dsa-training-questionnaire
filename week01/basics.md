# DSA Training Questionnaire

## Week 1: Basics of Programming

1. Make a basic calculator which inputs two numbers and an operator and outputs the desired result. Implement addition, subtraction, multiplication, division, and modulo operation

    - Example Output
        ```
        Return first number :10
        Enter Operator: +
        Enter Second Number: 100
        10 + 100 = 110
        ```
    - Try to also add a prompt if the operator is not supported
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
    - Try to implement power and factorial without using inbuilt functions. Make a different function for power and factorial and use them in the calculator

2. Input a number n. Print integers 1 to N, but print “Fizz” if an integer is divisible by 3, “Buzz” if an integer is divisible by 5, and “FizzBuzz” if an integer is divisible by both 3 and 5.

    - Example Output
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

3. Implement the function `int sumOfDigits(int num){}` which will take `num` as input in return the sum of the digits as output.

    - Eg: input = 12345; output = 1 + 2 + 3 + 4 + 5 = 15

4. Make a number guessing game, generate a random number [(might help)](https://www.journaldev.com/43739/random-number-generator-c-plus-plus#:~:text=Generate%20random%20numbers%20within%20a%20range&text=For%20instance%2C%20in%20order%20to,%2B%20(%20rand%20()%20%25%209)%3B) between 1 and 1000 and ask player to guess a number, if the player guesses correctly, display a congratulation message and exit. If the guess is incorrect, mention if the user guessed too high or too low.
    - Example Output
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
    - Now for the fun part, you can see that randomly checking is too long, how can you complete this game in minimum number of steps.
        <details><summary>Click me for a hint</summary>
        <p>

        google `binary search` (It's okay if you don't get a hang of it as we will discuss it in upcoming sessions, this is supposed to be a bit tricky so don't get sad)

        </p>
        </details>


