## Tutorials

GeeksforGeeks [sorting algorithms](https://www.geeksforgeeks.org/sorting-algorithms/)

Tutorialspoint Data Structures and Algorithms: [Sorting Algorithms](https://www.tutorialspoint.com/data_structures_algorithms/sorting_algorithms.htm)

brilliant.org [Sorting Algorithms](https://brilliant.org/wiki/sorting-algorithms/)

toptal.com [Sorting Algorithms](https://www.toptal.com/developers/sorting-algorithms)

## Solutions

#### Insertion Sort Challenges
###### Insertion Sort Part 1
[Description](https://www.hackerrank.com/challenges/insertionsort1/problem)

Java solution
```java
static void insertionSort1(int n, int[] arr) {
    int el = arr[n-1];
    int i = 0;
    while(arr[i] <= el){
        i++;
    }
    for(int j=n-1; j>i; j--){
        arr[j] = arr[j-1];
        for(int k:arr){
            System.out.print(k + " ");
        }
        System.out.println();
    }
    arr[i] = el;
        for(int k:arr){
            System.out.print(k + " ");
        }
        System.out.println();
}
```

###### Insertion Sort Part 2
[Description](https://www.hackerrank.com/challenges/insertionsort2/problem)

Java solution
```java
static void insertionSort2(int n, int[] arr) {
    for(int i=1; i<n; i++){
        int key = arr[i];
        int j=i-1;
        while(j>=0 && arr[j]>key){
            arr[j+1]=arr[j];
            j--;
        }
        arr[j+1]=key;
        for(int k:arr){
            System.out.print(k + " ");
        }
        System.out.println();
    }
}
```

###### Correctness and the Loop Invariant
[Description](https://www.hackerrank.com/challenges/correctness-invariant/problem)

more on [Loop Invariant](https://www.cs.scranton.edu/~mccloske/courses/cmps144/invariants_lec.html)

Java solution
```java
public static void insertionSort(int[] A){
    for(int i = 1; i < A.length; i++){
        int value = A[i];
        int j = i - 1;
        while(j >= 0 && A[j] > value){
            A[j + 1] = A[j];
            j = j - 1;
        }
        A[j + 1] = value;
    }

    printArray(A);
}
```


