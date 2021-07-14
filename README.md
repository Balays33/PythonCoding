# PythonCoding
 Python studying
 
0. assignment: Create a Tic Tac Toe game
requirements: 2 players should be able to play the game (both sitting at the same computer) The board should be printed out every time a player makes a move You should be able to accept input of the player position and then place a symbol on the board 

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


8. Reverse a String (solution) This problem is similar to the String Palindrome problem we have discussed above. If you can solve that problem, you can solve this as well. You can use indexOf() or substring() to reverse a String or alternatively, convert the problem to reverse an array by operating on character array instead of String. If you want to brush up your data structure skill you can also check Data Structures and Algorithms: Deep Dive Using Java course on Udemy before solving this question.

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

83. CountFactors

Count factors of given number n.

A positive integer D is a factor of a positive integer N if there exists an integer M such that N = D * M.

For example, 6 is a factor of 24, because M = 4 satisfies the above condition (24 = 6 * 4).

Write a function:

class Solution { public int solution(int N); }

that, given a positive integer N, returns the number of its factors.

For example, given N = 24, the function should return 8, because 24 has 8 factors, namely 1, 2, 3, 4, 6, 8, 12, 24. There are no other factors of 24.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..2,147,483,647].

84.MinPerimeterRectangle

      Find the minimal perimeter of any rectangle whose area equals N.

      An integer N is given, representing the area of some rectangle.

      The area of a rectangle whose sides are of length A and B is A * B, and the perimeter is 2 * (A + B).

      The goal is to find the minimal perimeter of any rectangle whose area equals N. The sides of this rectangle should be only integers.

      For example, given integer N = 30, rectangles of area 30 are:

      (1, 30), with a perimeter of 62,
      (2, 15), with a perimeter of 34,
      (3, 10), with a perimeter of 26,
      (5, 6), with a perimeter of 22.
      Write a function:

      class Solution { public int solution(int N); }

      that, given an integer N, returns the minimal perimeter of any rectangle whose area is exactly equal to N.

      For example, given an integer N = 30, the function should return 22, as explained above.

      Write an efficient algorithm for the following assumptions:

      N is an integer within the range [1..1,000,000,000].
      
Lesson 11 Sieve of Eratosthenes

87. CountSemiprimes

    Count the semiprime numbers in the given range [a..b] A prime is a positive integer X that has exactly two distinct divisors: 1 and X. The first few prime integers are 2, 3, 5, 7, 11 and 13.

    A semiprime is a natural number that is the product of two (not necessarily distinct) prime numbers. The first few semiprimes are 4, 6, 9, 10, 14, 15, 21, 22, 25, 26.

    You are given two non-empty arrays P and Q, each consisting of M integers. These arrays represent queries about the number of semiprimes within specified ranges.

    Query K requires you to find the number of semiprimes within the range (P[K], Q[K]), where 1 ≤ P[K] ≤ Q[K] ≤ N.

    For example, consider an integer N = 26 and arrays P, Q such that:

      P[0] = 1    Q[0] = 26
      P[1] = 4    Q[1] = 10
      P[2] = 16   Q[2] = 20
    The number of semiprimes within each of these ranges is as follows:

    (1, 26) is 10, (4, 10) is 4, (16, 20) is 0. Write a function:

    class Solution { public int[] solution(int N, int[] P, int[] Q); }

    that, given an integer N and two non-empty arrays P and Q consisting of M integers, returns an array consisting of M elements specifying the consecutive answers to all the queries.

    For example, given an integer N = 26 and arrays P, Q such that:

      P[0] = 1    Q[0] = 26
      P[1] = 4    Q[1] = 10
      P[2] = 16   Q[2] = 20
    the function should return the values [10, 4, 0], as explained above.

    Write an efficient algorithm for the following assumptions:

    N is an integer within the range [1..50,000]; M is an integer within the range [1..30,000]; each element of arrays P, Q is an integer within the range [1..N]; P[i] ≤ Q[i].
    
88. CountNonDivisible

      Calculate the number of elements of an array that are not divisors of each element.

      You are given an array A consisting of N integers.

      For each number A[i] such that 0 ≤ i < N, we want to count the number of elements of the array that are not the divisors of A[i]. We say that these elements are non-divisors.

      For example, consider integer N = 5 and array A such that:

          A[0] = 3
          A[1] = 1
          A[2] = 2
          A[3] = 3
          A[4] = 6
      For the following elements:

      A[0] = 3, the non-divisors are: 2, 6,
      A[1] = 1, the non-divisors are: 3, 2, 3, 6,
      A[2] = 2, the non-divisors are: 3, 3, 6,
      A[3] = 3, the non-divisors are: 2, 6,
      A[4] = 6, there aren't any non-divisors.
      Write a function:

      class Solution { public int[] solution(int[] A); }

      that, given an array A consisting of N integers, returns a sequence of integers representing the amount of non-divisors.

      Result array should be returned as an array of integers.

      For example, given:

          A[0] = 3
          A[1] = 1
          A[2] = 2
          A[3] = 3
          A[4] = 6
      the function should return [2, 4, 3, 2, 0], as explained above.

      Write an efficient algorithm for the following assumptions:

      N is an integer within the range [1..50,000];
      each element of array A is an integer within the range [1..2 * N].

Lesson 12 Euclidean algorithm

ChocolatesByNumbers
There are N chocolates in a circle. Count the number of chocolates you will eat.

Two positive integers N and M are given. Integer N represents the number of chocolates arranged in a circle, numbered from 0 to N − 1.

You start to eat the chocolates. After eating a chocolate you leave only a wrapper.

You begin with eating chocolate number 0. Then you omit the next M − 1 chocolates or wrappers on the circle, and eat the following one.

More precisely, if you ate chocolate number X, then you will next eat the chocolate with number (X + M) modulo N (remainder of division).

You stop eating when you encounter an empty wrapper.

For example, given integers N = 10 and M = 4. You will eat the following chocolates: 0, 4, 8, 2, 6.

The goal is to count the number of chocolates that you will eat, following the above rules.

Write a function:

class Solution { public int solution(int N, int M); }

that, given two positive integers N and M, returns the number of chocolates that you will eat.

For example, given integers N = 10 and M = 4. the function should return 5, as explained above.

Write an efficient algorithm for the following assumptions:

N and M are integers within the range [1..1,000,000,000].

90. CommonPrimeDivisors

      Check whether two numbers have the same prime divisors.

      A prime is a positive integer X that has exactly two distinct divisors: 1 and X. The first few prime integers are 2, 3, 5, 7, 11 and 13.

      A prime D is called a prime divisor of a positive integer P if there exists a positive integer K such that D * K = P. For example, 2 and 5 are prime divisors of 20.

      You are given two positive integers N and M. The goal is to check whether the sets of prime divisors of integers N and M are exactly the same.

      For example, given:

      N = 15 and M = 75, the prime divisors are the same: {3, 5};
      N = 10 and M = 30, the prime divisors aren't the same: {2, 5} is not equal to {2, 3, 5};
      N = 9 and M = 5, the prime divisors aren't the same: {3} is not equal to {5}.
      Write a function:

      class Solution { public int solution(int[] A, int[] B); }

      that, given two non-empty arrays A and B of Z integers, returns the number of positions K for which the prime divisors of A[K] and B[K] are exactly the same.

      For example, given:

          A[0] = 15   B[0] = 75
          A[1] = 10   B[1] = 30
          A[2] = 3    B[2] = 5
      the function should return 1, because only one pair (15, 75) has the same set of prime divisors.

      Write an efficient algorithm for the following assumptions:

      Z is an integer within the range [1..6,000];
      each element of arrays A, B is an integer within the range [1..2,147,483,647].
      
91. AbsDistinct

Compute number of distinct absolute values of sorted array elements.

A non-empty array A consisting of N numbers is given. The array is sorted in non-decreasing order. The absolute distinct count of this array is the number of distinct absolute values among the elements of the array.

For example, consider array A such that:

A[0] = -5 A[1] = -3 A[2] = -1 A[3] = 0 A[4] = 3 A[5] = 6 The absolute distinct count of this array is 5, because there are 5 distinct absolute values among the elements of this array, namely 0, 1, 3, 5 and 6.

Write a function:

class Solution { public int solution(int[] A); }

that, given a non-empty array A consisting of N numbers, returns absolute distinct count of array A.

For example, given array A such that:

A[0] = -5 A[1] = -3 A[2] = -1 A[3] = 0 A[4] = 3 A[5] = 6 the function should return 5, as explained above.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..100,000]; each element of array A is an integer within the range [−2,147,483,648..2,147,483,647]; array A is sorted in non-decreasing order.

92. CountTriangles

  Count the number of triangles that can be built from a given set of edges.

  An array A consisting of N integers is given. A triplet (P, Q, R) is triangular if it is possible to build a triangle with sides of lengths A[P], A[Q] and A[R]. In other words, triplet (P, Q, R) is triangular if 0 ≤ P < Q < R < N and:

  A[P] + A[Q] > A[R],
  A[Q] + A[R] > A[P],
  A[R] + A[P] > A[Q].
  For example, consider array A such that:

    A[0] = 10    A[1] = 2    A[2] = 5
    A[3] = 1     A[4] = 8    A[5] = 12
  There are four triangular triplets that can be constructed from elements of this array, namely (0, 2, 4), (0, 2, 5), (0, 4, 5), and (2, 4, 5).

  Write a function:

  class Solution { public int solution(int[] A); }

  that, given an array A consisting of N integers, returns the number of triangular triplets in this array.

  For example, given array A such that:

    A[0] = 10    A[1] = 2    A[2] = 5
    A[3] = 1     A[4] = 8    A[5] = 12
  the function should return 4, as explained above.

  Write an efficient algorithm for the following assumptions:

  N is an integer within the range [0..1,000];
  each element of array A is an integer within the range [1..1,000,000,000].

97. CountTriangles

Count the number of triangles that can be built from a given set of edges.

An array A consisting of N integers is given. A triplet (P, Q, R) is triangular if it is possible to build a triangle with sides of lengths A[P], A[Q] and A[R]. In other words, triplet (P, Q, R) is triangular if 0 ≤ P < Q < R < N and:

A[P] + A[Q] > A[R], A[Q] + A[R] > A[P], A[R] + A[P] > A[Q]. For example, consider array A such that:

A[0] = 10    A[1] = 2    A[2] = 5
A[3] = 1     A[4] = 8    A[5] = 12
There are four triangular triplets that can be constructed from elements of this array, namely (0, 2, 4), (0, 2, 5), (0, 4, 5), and (2, 4, 5).

Write a function:

class Solution { public int solution(int[] A); }

that, given an array A consisting of N integers, returns the number of triangular triplets in this array.

For example, given array A such that:

A[0] = 10    A[1] = 2    A[2] = 5
A[3] = 1     A[4] = 8    A[5] = 12
the function should return 4, as explained above.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [0..1,000]; each element of array A is an integer within the range [1..1,000,000,000].

MinAbsSumOfTwo
Find the minimal absolute value of a sum of two elements.

Let A be a non-empty array consisting of N integers.

The abs sum of two for a pair of indices (P, Q) is the absolute value |A[P] + A[Q]|, for 0 ≤ P ≤ Q < N.

For example, the following array A:

 A[0] =  1
 A[1] =  4
 A[2] = -3
has pairs of indices (0, 0), (0, 1), (0, 2), (1, 1), (1, 2), (2, 2). The abs sum of two for the pair (0, 0) is A[0] + A[0] = |1 + 1| = 2. The abs sum of two for the pair (0, 1) is A[0] + A[1] = |1 + 4| = 5. The abs sum of two for the pair (0, 2) is A[0] + A[2] = |1 + (−3)| = 2. The abs sum of two for the pair (1, 1) is A[1] + A[1] = |4 + 4| = 8. The abs sum of two for the pair (1, 2) is A[1] + A[2] = |4 + (−3)| = 1. The abs sum of two for the pair (2, 2) is A[2] + A[2] = |(−3) + (−3)| = 6. Write a function:

class Solution { public int solution(int[] A); }

that, given a non-empty array A consisting of N integers, returns the minimal abs sum of two for any pair of indices in this array.

For example, given the following array A:

 A[0] =  1
 A[1] =  4
 A[2] = -3
the function should return 1, as explained above.

Given array A:

 A[0] = -8
 A[1] =  4
 A[2] =  5
 A[3] =-10
 A[4] =  3
the function should return |(−8) + 5| = 3.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..100,000]; each element of array A is an integer within the range [−1,000,000,000..1,000,000,000].

100.TieRopes
Tie adjacent ropes to achieve the maximum number of ropes of length >= K.

There are N ropes numbered from 0 to N − 1, whose lengths are given in an array A, lying on the floor in a line. For each I (0 ≤ I < N), the length of rope I on the line is A[I].

We say that two ropes I and I + 1 are adjacent. Two adjacent ropes can be tied together with a knot, and the length of the tied rope is the sum of lengths of both ropes. The resulting new rope can then be tied again.

For a given integer K, the goal is to tie the ropes in such a way that the number of ropes whose length is greater than or equal to K is maximal.

For example, consider K = 4 and array A such that:

   A[0] = 1
   A[1] = 2
   A[2] = 3
   A[3] = 4
   A[4] = 1
   A[5] = 1
   A[6] = 3
The ropes are shown in the figure below.

We can tie:

rope 1 with rope 2 to produce a rope of length A[1] + A[2] = 5; rope 4 with rope 5 with rope 6 to produce a rope of length A[4] + A[5] + A[6] = 5. After that, there will be three ropes whose lengths are greater than or equal to K = 4. It is not possible to produce four such ropes.

Write a function:

class Solution { public int solution(int K, int[] A); }

that, given an integer K and a non-empty array A of N integers, returns the maximum number of ropes of length greater than or equal to K that can be created.

For example, given K = 4 and array A such that:

   A[0] = 1
   A[1] = 2
   A[2] = 3
   A[3] = 4
   A[4] = 1
   A[5] = 1
   A[6] = 3
the function should return 3, as explained above.

Write an efficient algorithm for the following assumptions:

N is an integer within the range [1..100,000]; K is an integer within the range [1..1,000,000,000]; each element of array A is an integer within the range [1..1,000,000,000].


101. Two Sum

     Given an array of integers, return indices of the two numbers such that they add up to a specific target.

     You may assume that each input would have exactly one solution, and you may not use the same element twice.

     Example:

     Given nums = [2, 7, 11, 15], target = 9,

     Because nums[0] + nums[1] = 2 + 7 = 9,
     return [0, 1]

102. Max Consecutive Ones

   Given a binary array, find the maximum number of consecutive 1s in this array.

   Example 1:
   Input: [1,1,0,1,1,1]
   Output: 3
   Explanation: The first two digits or the last three digits are consecutive 1s.
       The maximum number of consecutive 1s is 3.
   Note:

   The input array will only contain 0 and 1.
   The length of input array is a positive integer and will not exceed 10,000

103. Number Complement

    Given a positive integer, output its complement number. The complement strategy is to flip the bits of its binary representation. Example 1:

    Input: 5 Output: 2 Explanation: The binary representation of 5 is 101 (no leading zero bits), and its complement is 010. So you need to output 2.

    Example 2:

    Input: 1 Output: 0 Explanation: The binary representation of 1 is 1 (no leading zero bits), and its complement is 0. So you need to output 0.

    Note:

    The given integer is guaranteed to fit within the range of a 32-bit signed integer. You could assume no leading zero bit in the integer’s binary representation. This question is the same as 1009: https://leetcode.com/problems/complement-of-base-10-integer/
    
104. Hamming Distance

     The Hamming distance between two integers is the number of positions at which the corresponding bits are different.

     Given two integers x and y, calculate the Hamming distance.

     Note: 0 ≤ x, y < 231.

     Example:

     Input: x = 1, y = 4

     Output: 2

     Explanation: 1 (0 0 0 1) 4 (0 1 0 0) ↑ ↑

     The above arrows point to positions where the corresponding bits are different.
     
105. Palindrome Number

     Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.

     Example 1:

     Input: 121 Output: true Example 2:

     Input: -121 Output: false Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome. Example 3:

     Input: 10 Output: false Explanation: Reads 01 from right to left. Therefore it is not a palindrome.
     
106. Merge Sorted Array

    Given two sorted integer arrays nums1 and nums2, merge nums2 into nums1 as one sorted array.

    Note:

    The number of elements initialized in nums1 and nums2 are m and n respectively. You may assume that nums1 has enough space (size that is greater or equal to m + n) to hold additional elements from nums2. Example:

    Input: nums1 = [1,2,3,0,0,0], m = 3 nums2 = [2,5,6], n = 3

    Output: [1,2,2,3,5,6]
   
107.Jewels and Stones

     You're given strings J representing the types of stones that are jewels, and S representing the stones you have. Each character in S is a type of stone you have. You want to know how many of the stones you have are also jewels.

     The letters in J are guaranteed distinct, and all characters in J and S are letters. Letters are case sensitive, so "a" is considered a different type of stone from "A".

     Example 1:

     Input: J = "aA", S = "aAAbbbb" Output: 3 Example 2:

     Input: J = "z", S = "ZZ" Output: 0 Note:

     S and J will consist of letters and have length at most 50. The characters in J are distinct.
     
108. 3Sum

    Given an array nums of n integers, are there elements a, b, c in nums such that a + b + c = 0? Find all unique triplets in the array which gives the sum of zero.

    Note:

    The solution set must not contain duplicate triplets.

    Example:

    Given array nums = [-1, 0, 1, 2, -1, -4],

    A solution set is: [ [-1, 0, 1], [-1, -1, 2] ]

109.  Pascal's Triangle
     Given a non-negative integer numRows, generate the first numRows of Pascal's triangle.

     In Pascal's triangle, each number is the sum of the two numbers directly above it.

     Example:

     Input: 5 Output: [ [1], [1,1], [1,2,1], [1,3,3,1], [1,4,6,4,1] ]
     
110. 10. Product of Array Except Self

    Given an array nums of n integers where n > 1,  return an array output such that output[i] is equal to the product of all the elements of nums except nums[i].

    Example:

    Input:  [1,2,3,4]
    Output: [24,12,8,6]
    Constraint: It's guaranteed that the product of the elements of any prefix or suffix of the array (including the whole array) fits in a 32 bit integer.

    Note: Please solve it without division and in O(n).

    Follow up:
    Could you solve it with constant space complexity? (The output array does not count as extra space for the purpose of space complexity analysis.)

111. Largest Number At Least Twice of Others

     In a given integer array nums, there is always exactly one largest element.

     Find whether the largest element in the array is at least twice as much as every other number in the array.

     If it is, return the index of the largest element, otherwise return -1.

     Example 1:

     Input: nums = [3, 6, 1, 0] Output: 1 Explanation: 6 is the largest integer, and for every other number in the array x, 6 is more than twice as big as x. The index of value 6 is 1, so we return 1.

     Example 2:

     Input: nums = [1, 2, 3, 4] Output: -1 Explanation: 4 isn't at least as big as twice the value of 3, so we return -1.

     Note:

     nums will have a length in the range [1, 50]. Every nums[i] will be an integer in the range [0, 99].

112. Sort an Array

    Given an array of integers nums, sort the array in ascending order. Example 1:

    Input: nums = [5,2,3,1] Output: [1,2,3,5] Example 2:

    Input: nums = [5,1,1,2,0,0] Output: [0,0,1,1,2,5]

    Constraints:

    1 <= nums.length <= 50000 -50000 <= nums[i] <= 50000
    
113.Subarray Sum Equals K

   Given an array of integers and an integer k, you need to find the total number of continuous subarrays whose sum equals to k.

   Example 1:

   Input:nums = [1,1,1], k = 2 Output: 2

   Constraints:

   The length of the array is in range [1, 20,000]. The range of numbers in the array is [-1000, 1000] and the range of the integer k is [-1e7, 1e7].
   
114.Two Sum II - Input array is sorted

  Given an array of integers that is already sorted in ascending order, find two numbers such that they add up to a specific target number.

  The function twoSum should return indices of the two numbers such that they add up to the target, where index1 must be less than index2.

  Note:

  Your returned answers (both index1 and index2) are not zero-based. You may assume that each input would have exactly one solution and you may not use the same element twice. Example:

  Input: numbers = [2,7,11,15], target = 9 Output: [1,2] Explanation: The sum of 2 and 7 is 9. Therefore index1 = 1, index2 = 2.  
  
115. Sort Colors

   Given an array with n objects colored red, white or blue, sort them in-place so that objects of the same color are adjacent, with the colors in the order red, white and blue.

   Here, we will use the integers 0, 1, and 2 to represent the color red, white, and blue respectively.

   Note: You are not suppose to use the library's sort function for this problem.

   Example:

   Input: [2,0,2,1,1,0] Output: [0,0,1,1,2,2] Follow up:

   A rather straight forward solution is a two-pass algorithm using counting sort. First, iterate the array counting number of 0's, 1's, and 2's, then overwrite array with total number of 0's, then 1's and followed by 2's. Could you come up with a one-pass algorithm using only constant space?
   
116. 4Sum

    Given an array nums of n integers and an integer target, are there elements a, b, c, and d in nums such that a + b + c + d = target? Find all unique quadruplets in the array which gives the sum of target.

    Note:

    The solution set must not contain duplicate quadruplets.

    Example:

    Given array nums = [1, 0, -1, 0, -2, 2], and target = 0.

    A solution set is:
    [
      [-1,  0, 0, 1],
      [-2, -1, 1, 2],
      [-2,  0, 0, 2]
    ]
117. Container With Most Water

    Given n non-negative integers a1, a2, ..., an , where each represents a point at coordinate (i, ai). n vertical lines are drawn such that the two endpoints of line i is at (i, ai) and (i, 0). Find two lines, which together with x-axis forms a container, such that the container contains the most water.

    Note: You may not slant the container and n is at least 2.





    The above vertical lines are represented by array [1,8,6,2,5,4,8,3,7]. In this case, the max area of water (blue section) the container can contain is 49.



    Example:

    Input: [1,8,6,2,5,4,8,3,7]
    Output: 49

118. Container With Most Water

Given n non-negative integers a1, a2, ..., an , where each represents a point at coordinate (i, ai). n vertical lines are drawn such that the two endpoints of line i is at (i, ai) and (i, 0). Find two lines, which together with x-axis forms a container, such that the container contains the most water.

Note: You may not slant the container and n is at least 2.

The above vertical lines are represented by array [1,8,6,2,5,4,8,3,7]. In this case, the max area of water (blue section) the container can contain is 49.

Example:

Input: [1,8,6,2,5,4,8,3,7] Output: 49

119. Find the Duplicate Number

    Given an array nums containing n + 1 integers where each integer is between 1 and n (inclusive), prove that at least one duplicate number must exist. Assume that there is only one duplicate number, find the duplicate one.

    Example 1:

    Input: [1,3,4,2,2]
    Output: 2
    Example 2:

    Input: [3,1,3,4,2]
    Output: 3
    Note:

    You must not modify the array (assume the array is read only).
    You must use only constant, O(1) extra space.
    Your runtime complexity should be less than O(n2).
    There is only one duplicate number in the array, but it could be repeated more than once.
    
123. Plus One

   Given a non-empty array of digits representing a non-negative integer, increment one to the integer.

   The digits are stored such that the most significant digit is at the head of the list, and each element in the array contains a single digit.

   You may assume the integer does not contain any leading zero, except the number 0 itself.

   Example 1:

   Input: [1,2,3] Output: [1,2,4] Explanation: The array represents the integer 123. Example 2:

   Input: [4,3,2,1] Output: [4,3,2,2] Explanation: The array represents the integer 4321.

124. Prison Cells After N Days

   There are 8 prison cells in a row, and each cell is either occupied or vacant.

   Each day, whether the cell is occupied or vacant changes according to the following rules:

   If a cell has two adjacent neighbors that are both occupied or both vacant, then the cell becomes occupied. Otherwise, it becomes vacant. (Note that because the prison is a row, the first and the last cells in the row can't have two adjacent neighbors.)

   We describe the current state of the prison in the following way: cells[i] == 1 if the i-th cell is occupied, else cells[i] == 0.

   Given the initial state of the prison, return the state of the prison after N days (and N such changes described above.)

   Example 1:

   Input: cells = [0,1,0,1,1,0,0,1], N = 7 Output: [0,0,1,1,0,0,0,0] Explanation: The following table summarizes the state of the prison on each day: Day 0: [0, 1, 0, 1, 1, 0, 0, 1] Day 1: [0, 1, 1, 0, 0, 0, 0, 0] Day 2: [0, 0, 0, 0, 1, 1, 1, 0] Day 3: [0, 1, 1, 0, 0, 1, 0, 0] Day 4: [0, 0, 0, 0, 0, 1, 0, 0] Day 5: [0, 1, 1, 1, 0, 1, 0, 0] Day 6: [0, 0, 1, 0, 1, 1, 0, 0] Day 7: [0, 0, 1, 1, 0, 0, 0, 0]

   Example 2:

   Input: cells = [1,0,0,1,0,0,1,0], N = 1000000000 Output: [0,0,1,1,1,1,1,0]

129. Rotate Array

   Given an array, rotate the array to the right by k steps, where k is non-negative.

   Follow up:

   Try to come up as many solutions as you can, there are at least 3 different ways to solve this problem. Could you do it in-place with O(1) extra space?

   Example 1:

   Input: nums = [1,2,3,4,5,6,7], k = 3 Output: [5,6,7,1,2,3,4] Explanation: rotate 1 steps to the right: [7,1,2,3,4,5,6] rotate 2 steps to the right: [6,7,1,2,3,4,5] rotate 3 steps to the right: [5,6,7,1,2,3,4] Example 2:

   Input: nums = [-1,-100,3,99], k = 2 Output: [3,99,-1,-100] Explanation: rotate 1 steps to the right: [99,-1,-100,3] rotate 2 steps to the right: [3,99,-1,-100]

   Constraints:

   1 <= nums.length <= 2 * 10^4 It's guaranteed that nums[i] fits in a 32 bit-signed integer. k >= 0
  
130. Fizz Buzz

     Write a program that outputs the string representation of numbers from 1 to n.

     But for multiples of three it should output “Fizz” instead of the number and for the multiples of five output “Buzz”. For numbers which are multiples of both three and five output “FizzBuzz”.

     Example:

     n = 15,

     Return: [ "1", "2", "Fizz", "4", "Buzz", "Fizz", "7", "8",
     "Fizz", "Buzz", "11", "Fizz", "13", "14", "FizzBuzz" ]
     
 131. Reverse Integer

  Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

  Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

  Example 1:

  Input: x = 123 Output: 321 Example 2:

  Input: x = -123 Output: -321 Example 3:

  Input: x = 120 Output: 21 Example 4:

  Input: x = 0 Output: 0

  Constraints:

  -231 <= x <= 231 - 1
  
 132.  Roman to Integer

    Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M.

    Symbol       Value
    I             1
    V             5
    X             10
    L             50
    C             100
    D             500
    M             1000
    For example, 2 is written as II in Roman numeral, just two one's added together. 12 is written as XII, which is simply X + II. The number 27 is written as XXVII, which is XX + V + II.

    Roman numerals are usually written largest to smallest from left to right. However, the numeral for four is not IIII. Instead, the number four is written as IV. Because the one is before the five we subtract it making four. The same principle applies to the number nine, which is written as IX. There are six instances where subtraction is used:

    I can be placed before V (5) and X (10) to make 4 and 9. 
    X can be placed before L (50) and C (100) to make 40 and 90. 
    C can be placed before D (500) and M (1000) to make 400 and 900.
    Given a roman numeral, convert it to an integer.



    Example 1:

    Input: s = "III"
    Output: 3
    Example 2:

    Input: s = "IV"
    Output: 4
    Example 3:

    Input: s = "IX"
    Output: 9
    Example 4:

    Input: s = "LVIII"
    Output: 58
    Explanation: L = 50, V= 5, III = 3.
    Example 5:

    Input: s = "MCMXCIV"
    Output: 1994
    Explanation: M = 1000, CM = 900, XC = 90 and IV = 4.


    Constraints:

    1 <= s.length <= 15
    s contains only the characters ('I', 'V', 'X', 'L', 'C', 'D', 'M').
    It is guaranteed that s is a valid roman numeral in the range [1, 3999].
   
133.Reverse String

Example 1:

Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
Example 2:

Input: s = ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]
 

Constraints:

1 <= s.length <= 105
s[i] is a printable ascii character.
 

Follow up: Do not allocate extra space for another array. You must do this by modifying the input array in-place with O(1) extra memory.

134.Backspace String Compare

Share Given two strings s and t, return true if they are equal when both are typed into empty text editors. '#' means a backspace character.

Note that after backspacing an empty text, the text will continue empty.

Example 1:

Input: s = "ab#c", t = "ad#c" Output: true Explanation: Both s and t become "ac". Example 2:

Input: s = "ab##", t = "c#d#" Output: true Explanation: Both s and t become "". Example 3:

Input: s = "a##c", t = "#a#c" Output: true Explanation: Both s and t become "c". Example 4:

Input: s = "a#c", t = "b" Output: false Explanation: s becomes "c" while t becomes "b".

Constraints:

1 <= s.length, t.length <= 200 s and t only contain lowercase letters and '#' characters.

Follow up: Can you solve it in O(n) time and O(1) space?
