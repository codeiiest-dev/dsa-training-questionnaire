# DSA Training Questionnaire

## Week 1: Basics of Programming

Find the Time Complexities of the following functions

1.  ```cpp
    int sum(int a, int b){
        return a + b;
    }
    ```

    <details><summary>Click here for answer and hint</summary>

    -   Answer is O(n)
    -   It's because only one addition operation is taking place and returned to caller function

    </details>

2.  ```cpp
     bool isPrime(int n){
         for (int i = 2; i * i <= n; i++)
             if (n % i == 0)
                 return false;
         return true;
     }
    ```

    <details><summary>Click here for answer and hint</summary>

    -   Answer is ![](https://www.bruot.org/tex2img/media/k918C1WqOX5soeSiwsBZnq3jkFvLJOjb5DQ0hwOp2qez/tex2img_equation.png)
    -   It's because the loop variable at worst can go to ![](https://www.bruot.org/tex2img/media/k918C1WqOX5soeSiwsBZnq3jkFvLJOjb5DQ0hwOp2qez/tex2img_equation.png)

    </details>

3.  ```cpp
    int sumBits(int n){
        int sum = 0;
        while (n){
            sum += n % 2;
            n /= 2;
        }
        return sum;
    }
    ```

    <details><summary>Click here for answer and hint</summary>

    -   Answer is ![](https://www.bruot.org/tex2img/media/jhnQg6n1ChKFrPnNnhOZHCdKXgBGFmRAM8z7lSJfJfbB/tex2img_equation.png)
    -   It's because the loop will go through alll the bits of n, and we know that n will have at max ![](https://www.bruot.org/tex2img/media/jhnQg6n1ChKFrPnNnhOZHCdKXgBGFmRAM8z7lSJfJfbB/tex2img_equation.png) digits in binary format.
    -   [Here's a simple refresher about basics of binary number system](https://arith-matic.com/notebook/binary-numbers)

    </details>

-   You might need to revise [C style arrays](https://learning.rc.virginia.edu/courses/cpp_introduction/c_arrays/) for the follwoing two questions

4.  ```cpp
    bool nested_two_sum(int arr[], int arr_size, int target){
        for (int i = 0; i < arr_size; i++)
            for (int j = i + 1; j < arr_size; i++)
                if (arr[i] + arr[j] == target)
                    return true;
        return false;
    }
    ```

    <details><summary>Click here for answer and hint</summary>

    -   Answer is O(n^2)
    -   Explanation
        -   for i = 0, j will go 1,2,3,4...(n - 1) -> (n - 1) steps
        -   for i = 1, j will go 2,3,4,5...(n - 1) -> (n - 2) steps
        -   for i = 2, j will go 3,4,5,6...(n - 1) -> (n - 3) steps
        -   For every i, j loop will go through i + 1, i + 2,...(n - 1) -> (n - i - 1) steps
        -   So Total Number of Steps = ![](https://www.bruot.org/tex2img/media/SuWnfOZJE8XJaC36AIjEeXm5L1GUlAv4WrFxl0dIXs69/tex2img_equation.png)
        -   which equals (skipping some steps) ![](https://www.bruot.org/tex2img/media/a2kMlrOGeQHz5iaDLWNu7ZceLyyzX2BMBH8npxO4tS0b/tex2img_equation.png)

    </details>

5.  ```cpp
    int binary_search(int arr[], int arr_size, int target){
        int left = 0;
        int right = arr_size - 1;
        while (left <= right){
            int mid = left + (right - left) / 2;
            if (arr[mid] == target)
                return mid;
            else if (arr[mid] > target)
                right = mid - 1;
            else
                left = mid + 1;
        }
        return -1;
    }
    ```

    <details><summary>Click here for answer and hint</summary>

    -   Answer is ![](https://www.bruot.org/tex2img/media/jhnQg6n1ChKFrPnNnhOZHCdKXgBGFmRAM8z7lSJfJfbB/tex2img_equation.png)
    -   Refer [here](https://www.geeksforgeeks.org/complexity-analysis-of-binary-search/) for the detailed explaination

    </details>
