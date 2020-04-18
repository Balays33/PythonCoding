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
