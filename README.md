# PythonCoding
 Python studying


1. Fibonacci series (solution)
Write a simple Python program which will print Fibonacci series, e.g. 1 1 2 3 5 8 13 ... . up to a given number. We prepare for cross questions like using iteration over recursion and how to optimize the solution using caching and memoization.

2. A prime number (solution)
Write a Python program to check if a given number is prime or not. Remember, a prime number is a number which is not divisible by any other number, e.g. 3, 5, 7, 11, 13, 17, etc. Be prepared for cross, e.g. checking till the square root of a number, etc.

3. String Palindrome (solution)
You need to write a simple Python program to check if a given String is palindrome or not. A Palindrome is a String which is equal to the reverse of itself, e.g., "Bob" is a palindrome because of the reverse of "Bob" is also "Bob."  Though be prepared with both recursive and iterative solution of this problem. The interviewer may ask you to solve without using any library method, e.g. indexOf() or subString() so be prepared for that.

4. Integer Palindrome (solution)
This is generally asked as follow-up or alternative of the previous program. This time you need to check if given Integer is palindrome or not. An integer is called palindrome if it's equal to its reverse, e.g. 1001 is a palindrome, but 1234 is not because the reverse of 1234 is 4321 which is not equal to 1234. You can use divide by 10 to reduce the number and modulus 10 to get the last digit. This trick is used to solve this problem.

5. Armstrong number (solution)
A number is called an Armstrong number if it is equal to the cube of its every digit. For example, 153 is an Armstrong number because of 153= 1+ 125+27, which is equal to 1^3+5^3+3^3. You need to write a program to check if the given number is Armstrong number or not.

6. Avoiding deadlock in Python (solution)
This is one of the interesting programs from Java Interviews, mostly asked to 2 to 3 years of experienced programmers or higher. The interviewer simply asked you to write code where a resource is accessed by multiple threads. You need to write code in such a way that no deadlock should occur. The trick to solving this problem is acquiring resources in order and release them in reverse order, e.g. first acquire resource R1 and only if you have got R1 to go for R2. This way, you can avoid deadlock.




72. Triangle

      An array A consisting of N integers is given. A triplet (P, Q, R) is triangular if 0 ≤ P < Q < R < N and:

      A[P] + A[Q] > A[R],
      A[Q] + A[R] > A[P],
      A[R] + A[P] > A[Q].
      For example, consider array A such that:

        A[0] = 10    A[1] = 2    A[2] = 5
        A[3] = 1     A[4] = 8    A[5] = 20
      Triplet (0, 2, 4) is triangular.

      Write a function:

      class Solution { public int solution(int[] A); }

      that, given an array A consisting of N integers, returns 1 if there exists a triangular 
      triplet for this array and returns 0 otherwise.

      For example, given array A such that:

        A[0] = 10    A[1] = 2    A[2] = 5
        A[3] = 1     A[4] = 8    A[5] = 20
      the function should return 1, as explained above. Given array A such that:

        A[0] = 10    A[1] = 50    A[2] = 5
        A[3] = 1
      the function should return 0.

      Write an efficient algorithm for the following assumptions:

      N is an integer within the range [0..100,000];
      each element of array A is an integer within the range [−2,147,483,648..2,147,483,647].








75. Fish

      N voracious fish are moving along a river. Calculate how many fish are alive.

      You are given two non-empty arrays A and B consisting of N integers. Arrays A and B represent N voracious fish in a river, ordered downstream along the flow of the river.

      The fish are numbered from 0 to N − 1. If P and Q are two fish and P < Q, then fish P is initially upstream of fish Q. Initially, each fish has a unique position.

      Fish number P is represented by A[P] and B[P]. Array A contains the sizes of the fish. All its elements are unique. Array B contains the directions of the fish. It contains only 0s and/or 1s, where:

      0 represents a fish flowing upstream, 1 represents a fish flowing downstream. If two fish move in opposite directions and there are no other (living) fish between them, they will eventually meet each other. Then only one fish can stay alive − the larger fish eats the smaller one. More precisely, we say that two fish P and Q meet each other when P < Q, B[P] = 1 and B[Q] = 0, and there are no living fish between them. After they meet:

      If A[P] > A[Q] then P eats Q, and P will still be flowing downstream, If A[Q] > A[P] then Q eats P, and Q will still be flowing upstream. We assume that all the fish are flowing at the same speed. That is, fish moving in the same direction never meet. The goal is to calculate the number of fish that will stay alive.

      For example, consider arrays A and B such that:

      A[0] = 4    B[0] = 0
      A[1] = 3    B[1] = 1
      A[2] = 2    B[2] = 0
      A[3] = 1    B[3] = 0
      A[4] = 5    B[4] = 0
      Initially all the fish are alive and all except fish number 1 are moving upstream. Fish number 1 meets fish number 2 and eats it, then it meets fish number 3 and eats it too. Finally, it meets fish number 4 and is eaten by it. The remaining two fish, number 0 and 4, never meet and therefore stay alive.

      Write a function:

      class Solution { public int solution(int[] A, int[] B); }

      that, given two non-empty arrays A and B consisting of N integers, returns the number of fish that will stay alive.

      For example, given the arrays shown above, the function should return 2, as explained above.

      Write an efficient algorithm for the following assumptions:

      N is an integer within the range [1..100,000]; each element of array A is an integer within the range [0..1,000,000,000]; each element of array B is an integer that can have one of the following values: 0, 1; the elements of A are all distinct.
      
82. MaxDoubleSliceSum

      Find the maximal sum of any double slice.

      A non-empty array A consisting of N integers is given.

      A triplet (X, Y, Z), such that 0 ≤ X < Y < Z < N, is called a double slice.

      The sum of double slice (X, Y, Z) is the total of A[X + 1] + A[X + 2] + ... + A[Y − 1] + A[Y + 1] + A[Y + 2] + ... + A[Z − 1].

      For example, array A such that:

      A[0] = 3
      A[1] = 2
      A[2] = 6
      A[3] = -1
      A[4] = 4
      A[5] = 5
      A[6] = -1
      A[7] = 2
      contains the following example double slices:

      double slice (0, 3, 6), sum is 2 + 6 + 4 + 5 = 17, double slice (0, 3, 7), sum is 2 + 6 + 4 + 5 − 1 = 16, double slice (3, 4, 5), sum is 0. The goal is to find the maximal sum of any double slice.

      Write a function:

      class Solution { public int solution(int[] A); }

      that, given a non-empty array A consisting of N integers, returns the maximal sum of any double slice.

      For example, given:

      A[0] = 3
      A[1] = 2
      A[2] = 6
      A[3] = -1
      A[4] = 4
      A[5] = 5
      A[6] = -1
      A[7] = 2
      the function should return 17, because no double slice of array A has a sum of greater than 17.

      Write an efficient algorithm for the following assumptions:

      N is an integer within the range [3..100,000]; each element of array A is an integer within the range [−10,000..10,000].
     
 Lesson 10 Prime and composite numbers

CountFactors

Count factors of given number n.

A positive integer D is a factor of a positive integer N if there exists an integer M such that N = D * M.

For example, 6 is a factor of 24, because M = 4 satisfies the above condition (24 = 6 * 4).

Write a function:

class Solution { public int solution(int N); }

that, given a positive integer N, returns the number of its factors.

For example, given N = 24, the function should return 8, because 24 has 8 factors, namely 1, 2, 3, 4, 6, 8, 12, 24. There are no other factors of 24.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..2,147,483,647].
