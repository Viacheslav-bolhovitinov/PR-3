#include <stdio.h>

int f(int r) {
    if (r == 1) {
        return 2;
    } else if (r == 2) {
        return 4;
    } else if (r == 3) {
        return 10;
    } else {
        return 2*f(r-1) - 2*f(r-2) + 2*f(r-3);
    }
}

int main() {
    int r;
    printf("Enter the number of digits: ");
    scanf("%d", &r);
    printf("Number of numbers with %d digits: %d\n", r, f(r));
    return 0;
}
