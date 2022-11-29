# binary_search_01
Binary Search is a searching algorithm used in a sorted array by repeatedly dividing the search interval in half. The idea of binary search is to use the information that the array is sorted and reduce the time complexity to O(Log n). 



public class Binary_search_Array {
    public static int binarySearch(int[] arr, int x) {
        //Your code goes here
        int start = 0;
        int end = arr.length - 1;
        int mid = start;
        while(start <= end)
        {
            mid = start + (end - start) / 2;
            if (arr[mid] > x) {
            end = mid - 1;
        }
        else if (arr[mid] < x) {
            start = mid + 1;
        }
        else {
            return mid;
        }
        }
        return -1;
    }

    public static void main(String[] args) {
        int arr[] = {1,4,7,10,20,35,40};
        int index = binarySearch(arr,20);
        System.out.println(index);
    }
}
