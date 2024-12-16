Definition: Recursion is a method where a function calls itself to solve smaller instances of a problem until a base condition is met.

Base Case: A condition to stop the recursion, preventing infinite loops and stack overflow.

Recursive Case: The part where the function calls itself, reducing the problem size with each call.

Stack Usage: Each recursive call is stored in the call stack, holding its parameters and local variables until completion.

Divide and Conquer: Many recursive problems use the divide-and-conquer approach, breaking problems into subproblems (e.g., merge sort, quicksort).

Common Problems: Recursion is used in problems like factorial, Fibonacci sequence, tree traversals, and backtracking algorithms.

Advantages: Simplifies code for problems with repetitive substructures (e.g., permutations, combinations).

Disadvantages: Can lead to high memory usage and stack overflow if not managed properly with large inputs.

Tail Recursion: A special form where the recursive call is the last operation in the function, optimizing stack usage in some languages.

Alternatives: Iterative solutions often use loops and are generally more memory-efficient compared to recursion.


a function 'a' returns to the function 'b' calling them after the function 'a' finishes

what is stack overflow?
    whenever theres no basecase then the function will call itself infinite times hence run into basecase.

--sequence matters look at q1 and q2
--solve for one and the others will solve on its own(?)
INTUITION
    1.base case 
    2.one code part which follows one test case

    
1 print n to 1
    cout<< n << " ";
    if(n==1)return;
    printTillOne(n-1);
    

2 print 1 to n
    if(n==0)return;
    printTillN(n-1);
    cout<< n <<" ";

3 factorial of n
    if(n==1)return ans;
    ans=ans*n;
    factorial(n-1);

4 fibonacci
    uve to find out fib(n-1)+fib(n-2)
    so jus call it 
    if(n<=1)return n;
    return fib(n-1)+fib(n-2);

5