source - geeksforgeeks

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

typical structure

    fun(){
        base case
        recursive call(change in parameter)
    }

applications of recursion- 
    1 dp
    2 backtracking
    3 divide and conquer

sirf base case pr return jatay
order matters in recursion 
    before call or after call

1 print n to 1

f(n){
    if(n==0)return
    print n;
    f(n-1)
}

2 print 1 to n

f(n){
    if(n==0)return
    f(n-1)
    print n
}

tail recursion - the last thing in the function should be the recursive call.

better(){ 
    base case
    print
    call
}

worse(){
    basecase
    call
    print
}

how to tail recursion - add a parameter

3 check if palindrome
    make a help func with help(0,n-1,s)
    check for every i and j and return 1 if i>=j else return 0