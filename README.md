# C-programming3

1.Write a c program to print all prime numbers between two limits.

```
#include <stdio.h>

int main() {
    int lower, upper, i, j, isPrime;

    printf("Enter lower limit: ");
    scanf("%d", &lower);

    printf("Enter upper limit: ");
    scanf("%d", &upper);

    printf("Prime numbers between %d and %d are:\n", lower, upper);

    for(i = lower; i <= upper; i++) {
        if(i < 2) continue; 

        isPrime = 1;

        for(j = 2; j <= i / 2; j++) {
            if(i % j == 0) {
                isPrime = 0;
                break;
            }
        }

        if(isPrime == 1) {
            printf("%d ", i);
        }
    }

    return 0;
}
```
#Output
<img width="478" height="237" alt="image" src="https://github.com/user-attachments/assets/6e83a09c-524b-4864-b8f4-065217d41cae" />

2. Write a c program to count the number of digits in a number.

```
#include <stdio.h>

int main() {
    int num, count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    if(num == 0) {
        count = 1;
    } else {
        if(num < 0) {
            num = -num;
        }

        while(num > 0) {
            num = num / 10;
            count++;
        }
    }

    printf("Number of digits = %d\n", count);

    return 0;
}
```
#Output

<img width="461" height="314" alt="image" src="https://github.com/user-attachments/assets/f17c7001-809b-499e-80be-65b322f7eb96" />

3. Write a c program to print the alphabet S in n x n matrix.

```
#include <stdio.h>

int main() {
    int n, i, j;

    printf("Enter value of n: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        for(j = 0; j < n; j++) {

            if (i == 0 ||                
                i == n/2 ||               
                i == n-1 ||               
                (j == 0 && i < n/2) ||   
                (j == n-1 && i > n/2))   
            {
                printf("* ");
            } else {
                printf("  ");
            }
        }
        printf("\n");
    }

    return 0;
}
```

#Output
<img width="483" height="349" alt="image" src="https://github.com/user-attachments/assets/22d7860e-60d7-4746-8388-adac9d5eb5dc" />

4.Write a c program to print the pyramid pattern.

```
#include <stdio.h>

int main() {
    int n = 4;  
    int i, j;

    for(i = 1; i <= n; i++) {


        for(j = 1; j <= n - i; j++) {
            printf(" ");
        }

        for(j = 1; j <= (2 * i - 1); j++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}
```
#Output
<img width="449" height="293" alt="image" src="https://github.com/user-attachments/assets/54427a03-2652-4b28-9bc2-5b533b242f82" />

5.Write a c program to find GCD of two numbers using loop.
```
#include <stdio.h>

int main() {
    int a, b, i, gcd;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    int min = (a < b) ? a : b;

    for(i = 1; i <= min; i++) {
        if(a % i == 0 && b % i == 0) {
            gcd = i;
        }
    }

    printf("GCD of %d and %d = %d\n", a, b, gcd);

    return 0;
}
```

#Output
<img width="564" height="284" alt="image" src="https://github.com/user-attachments/assets/ea06ead5-d835-443e-a8e9-f88b978a2c82" />
