# Activities

## Task 1

- Refer to the following link. Discuss how Merge-sort works:
  https://opendsa-server.cs.vt.edu/OpenDSA/AV/Sorting/mergesortAV.html
> (Group 6 answer: Merge sort subdivides the array into smaller subarrays until they are a single element long, then it compares the adjacent subarrays to see which element is smaller, merging them up to larger subarrays. These subarrays are then internally sorted, which means the algorithm can compare the first element of each subarray to merge the smaller element up into a larger subarray. This continues until the whole array is sorted.)

- Merge-sort Practice. Refer to the following link. Merge the two sub-arrays into the larger array.
  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Sorting/MergesortMergePRO.html

## Task 2

- Refer to the following link. Discuss how Quick-sort works:  
  https://opendsa-server.cs.vt.edu/OpenDSA/AV/Sorting/quicksortAV.html
> (Group 6 answer: The middle element is swapped to the end of the array to act as a pivot. The subarray to the left of the pivot is then partitioned, and the left bound of the subarray is moved right until it reaches a value that is greater than or equal to the pivot value. The right bound is then moved to the right until it reaches a value less than the pivot value. If the right bound has crossed the left bound, all elements to the left of the left bound are less than the pivot and all elements to the right of the right bound are greater than or equal to the pivot. The pivot is then swapped with the value where the bounds crossed. If the bounds didn't cross, the values at the left and right bounds are swapped and the left bound is then moved again, etc.. until the bounds cross. This swapping and partitioning is recursed until the partitioned subarrays are a single element in length, meaning they can be considered sorted and they are locked in place.)

- Quick-sort Practice. Refer to the following link. Partition the array using quicksort.
  https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/Sorting/QuicksortPartitPRO.html

## Task 3

- The following snippet is from `./src/quicksort.cpp` lines 32-43. Discuss in groups how the code works:

```cpp
void quickSort(int arr[], int low, int high)
{
    if (low < high) // check whether bounds have crossed
    {
        //partition the array
        int pivot = partition(arr, low, high); // partition the array and return new pivot

        //sort the sub arrays independently
        quickSort(arr, low, pivot - 1); // recurse with the subarrays around the pivot
        quickSort(arr, pivot + 1, high);
    }
}
```

- The following snippet is from `./src/quicksort.cpp` line 27. Discuss in groups how ìt works:

```cpp
swap(&arr[i + 1], &arr[high]); // swap the element at i+1 (smaller element + 1) and the pivot
```

## Task 4: Individual (at home)

1. Merge-sort has better worst case performance than quicksort. So why Quick-sort is considered better than Merge-sort? Refer to the following article
   https://www.geeksforgeeks.org/quicksort-better-mergesort/
> Quick sort is faster and requires less space - no additional storage space is needed to perform sorting. 


2. Refer to the following article. Analyze the complexity of the Merge-sort algorithm.
   https://www.softwaretestinghelp.com/merge-sort/
> "The total time to perform merge sort will be n (log n+1), which gives us the time complexity of O(n*log n). The time complexity for merge sort is the same in all three cases (worst, best and average)."



3. Refer to the following article. Analyze the complexity of the Quick-sort algorithm.
   https://www.softwaretestinghelp.com/quick-sort/
> Worst case  O(n2), Best case and Average O(n*log n)