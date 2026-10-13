# day--9-

#include <stdio.h>

int main() {
    int n, temp, digit, i;
    int fact, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    temp = n;

    while (temp > 0) {
        digit = temp % 10;
        fact = 1;

        for (i = 1; i <= digit; i++) {
            fact = fact * i;
        }

        sum = sum + fact;
        temp = temp / 10;
    }

    if (sum == n) {
        printf("%d is a Strong Number", n);
    } else {
        printf("%d is not a Strong Number", n);
    }

    return 0;
}

#include <stdio.h>

int main() {
    int n, i;
    int a[100];
    int largest, second;

    printf("Enter array size: ");
    scanf("%d", &n);

    printf("Enter array elements: ");
    for (i = 0; i < n; i++) {
        scanf("%d", &a[i]);
    }

    largest = second = -2147483647 - 1;

    for (i = 0; i < n; i++) {
        if (a[i] > largest) {
            second = largest;
            largest = a[i];
        } else if (a[i] > second && a[i] < largest) {
            second = a[i];
        }
    }

    if (second == -2147483647 - 1) {
        printf("Second largest element does not exist");
    } else {
        printf("Second largest element = %d", second);
    }

    return 0;
}

#include <stdio.h>

int main() {
    int n, temp, digit, reverse = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    temp = n;

    while (temp > 0) {
        digit = temp % 10;
        reverse = reverse * 10 + digit;
        temp = temp / 10;
    }

    printf("Reverse = %d\n", reverse);

    if (n == reverse) {
        printf("Palindrome Number");
    } else {
        printf("Not a Palindrome Number");
    }

    return 0;
}
