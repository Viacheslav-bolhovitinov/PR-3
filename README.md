#include <stdio.h>

int count_numbers(int n) {
    if (n == 1) {
        return 2; 
    } else if (n == 2) {
        return 4; 
    } else {
        int count = 0;
        count += 2 * count_numbers(n - 1); 
        count += 2 * count_numbers(n - 2); 
        return count;
    }
}

int main() {
    int n;
    scanf("%d", &n);

    printf("%d\n", count_numbers(n));

    return 0;
}
