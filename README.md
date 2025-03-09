# plsheets
#sheet2
// 1) Program to calculate max, min, and average of 10 numbers
#include <stdio.h>

int main() {
    int arr[10], i, max, min, sum = 0;
    float avg;

    printf("Enter 10 numbers: \n");
    for(i = 0; i < 10; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];
        if(i == 0) {
            max = min = arr[i];
        } else {
            if(arr[i] > max) max = arr[i];
            if(arr[i] < min) min = arr[i];
        }
    }

    avg = sum / 10.0;
    printf("Max: %d\nMin: %d\nAverage: %.2f\n", max, min, avg);
    return 0;
}

// 2) Function to check if array is sorted in ascending order
int isAscending(int arr[], int size) {
    for(int i = 0; i < size - 1; i++) {
        if(arr[i] > arr[i + 1]) {
            return 0; // not ascending
        }
    }
    return 1; // ascending
}

// 3) Sum of odd and even numbers
#include <stdio.h>

int main() {
    int arr[10], i, odd_sum = 0, even_sum = 0;
    printf("Enter 10 integers: \n");
    for(i = 0; i < 10; i++) {
        scanf("%d", &arr[i]);
        if(arr[i] % 2 == 0) even_sum += arr[i];
        else odd_sum += arr[i];
    }
    printf("Sum of even numbers: %d\nSum of odd numbers: %d\n", even_sum, odd_sum);
    return 0;
}

// 4) Determine array trend
#include <stdio.h>

int main() {
    int arr[10], i;
    int increasing = 1, decreasing = 1;

    printf("Enter 10 integers: \n");
    for(i = 0; i < 10; i++) {
        scanf("%d", &arr[i]);
    }

    for(i = 0; i < 9; i++) {
        if(arr[i] < arr[i + 1]) decreasing = 0;
        if(arr[i] > arr[i + 1]) increasing = 0;
    }

    if(increasing) printf("The numbers in the array are increasing\n");
    else if(decreasing) printf("The numbers in the array are decreasing\n");
    else printf("The numbers in the array are not changing\n");

    return 0;
}

// 5) Find position of a number in a 3x4 matrix
#include <stdio.h>

int main() {
    int matrix[3][4];
    int number, found = 0;

    printf("Enter elements of 3x4 matrix: \n");
    for(int i = 0; i < 3; i++) {
        for(int j = 0; j < 4; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    printf("Enter number to search: ");
    scanf("%d", &number);

    for(int i = 0; i < 3; i++) {
        for(int j = 0; j < 4; j++) {
            if(matrix[i][j] == number) {
                printf("Number found at position (%d, %d)\n", i, j);
                found = 1;
                break;
            }
        }
        if(found) break;
    }

    if(!found) printf("Number not found.\n");
    return 0;
}

// 6) Find row with maximum sum in matrix
#include <stdio.h>

int main() {
    int matrix[3][4];
    int maxSum = 0, maxRow = 0;

    printf("Enter elements of 3x4 matrix: \n");
    for(int i = 0; i < 3; i++) {
        int rowSum = 0;
        for(int j = 0; j < 4; j++) {
            scanf("%d", &matrix[i][j]);
            rowSum += matrix[i][j];
        }
        if(rowSum > maxSum) {
            maxSum = rowSum;
            maxRow = i;
        }
    }

    printf("Row with maximum sum is row %d with sum %d\n", maxRow, maxSum);
    return 0;
}

// 7) Display matrix pattern
#include <stdio.h>

int main() {
    int matrix[5][5];

    for(int i = 0; i < 5; i++) {
        for(int j = 0; j < 5; j++) {
            if(j < i) matrix[i][j] = -1;
            else if(i == j) matrix[i][j] = 0;
            else matrix[i][j] = 1;
        }
    }

    for(int i = 0; i < 5; i++) {
        for(int j = 0; j < 5; j++) {
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}

// More solutions will follow, let me know if you want adjustments so far!
