Definition : An array is a collection of elements, stored in contiguous memory locations, and accessible using indices.
Indexing: Elements are accessed using zero-based indexing (e.g., arr[0] for the first element).
Fixed Size: Arrays have a fixed size defined during declaration (e.g., int arr[5]).
Homogeneous Elements: All elements in an array must be of the same data type.
Insertion: Adding elements at the end is O(1), but inserting in the middle requires shifting (O(n)).
Deletion: Removing elements from the end is O(1), but deleting elsewhere involves shifting (O(n)).
Access Time: Direct access to any element is O(1) using its index.
Memory Efficiency: Arrays have low overhead but require contiguous memory, which can lead to fragmentation.
Dynamic Arrays: Some languages offer resizable arrays (e.g., std::vector in C++, ArrayList in Java).
Applications: Arrays are used in sorting, searching, and as building blocks for more complex data structures.

brute - 
better - 
best - 

1 largest element in array
    brute - sort and return the last index(nlogn)
    better - none
    best - simple for loop and variable max

2 second Largest Element 
    brute - sort and for loop from n-1 to 0 
    better - 2 for loops one for mx1 and one for mx2
    best - 1 for loop 
           2 variables - mx1 mx2

3 checkSorted?

    for(int i=0;i<=n;i++){
        if(nums[i]==nums[i+1%n])c++;
    }

4 remove duplicates
    brute - store inside a set data structure and then put into the existing array
    better - none
    best - 2 pointer approach
        i and j pointers

        i=0 j=1
        for(j to n){
            if(arr[i]!=arr[j]){
                arr[i+1]=arr[j]
                i++
            }
        }
        return i+1
        
5 rotate by k places      
    brute - rotate array one place inside a while(k--) loop
                rotate array one place - take first element temporary
            take a temp array from 0 to k
            store 0 to k in temp 
            then put in array after k elemens using    
                for(i=d,i< n,i++){
                    a[i-d]=a[i]
                }
            then put in temp 
            int j=0
            for(i=k-n;i<n ;i++ ){
                arr[i]=temp[j]
                j++  
            }
    better - none
    best -
        int n=nums.size();
        k = k % n; 
        reverse(nums.begin(),nums.begin()+n-k);
        reverse(nums.begin()+n-k,nums.end());
        reverse(nums.begin(),nums.end());

6 move zeroes to end

    brute - take a temporary array and put all zeroes inside it
            put all elements of temp arr and put in normal arr
            fill the remaining array with 0s
    better - 
    best - 
        use 2 pointer j-to traverse i-to put zeroes
        if(arr[j]!=0)arr[i]=arr[j] i++
        then put zeroes from i to n-1
