# Count Positive Numbers in an Array (C)

## Description
This C program counts the number of positive integers present in an array and displays the result.

## How It Works
1. An integer array is defined in `main()`.
2. The array and its size are passed to the `count()` function.
3. The function iterates through the array using a loop.
4. Each positive number (`> 0`) increases the counter by 1.
5. The total count is returned and printed.

## Source Code

```c
#include <stdio.h>

int count(int a[], int n) {
    int number = 0;

    for (int i = 0; i < n; i++) {
        if (a[i] > 0) {
            number++;
        }
    }

    return number;
}

int main() {
    int a[] = {1, 2, -3, -4, 5, 6, 7};

    printf("The number of positive integers are %d", count(a, 7));

    return 0;
}
```

## Sample Input

```c
int a[] = {1, 2, -3, -4, 5, 6, 7};
```

## Sample Output

```
The number of positive integers are 5
```

## Time Complexity

```
O(n)
```

The array is traversed once.

## Space Complexity

```
O(1)
```

Only a single counter variable is used.

## Concepts Used

- Arrays
- Functions
- Loops (`for`)
- Conditional Statements (`if`)
- Counting Elements

## Note

In your original code:

```c
return number++;
```

it is better to write:

```c
return number;
```

because `number++` returns the current value of `number` and increments it afterward, but that increment is discarded when the function exits.
