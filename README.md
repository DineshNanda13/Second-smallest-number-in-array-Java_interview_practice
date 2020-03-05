# Second-smallest-number-in-array-Java_interview_practice
Java program to find the second smallest number in array
package second_Smallest;

/**
 *
 * @author Dinesh Nanda
 */

public class SecondSmallestInArray {

    public static void main(String[] args) {

        int arr[] = {1, 2, 5, 6, 3, 2};

        for (int i = 0; i < arr.length; i++) {
            for (int j = i + 1; j < arr.length; j++) {

                if (arr[i] > arr[j]) {
                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
        for (int i = 0; i < arr.length; i++) {
            if (i == 1) {
                System.out.print("Second smallest number in array is: "+arr[i]);
                break;
            }
        }
    }

}
