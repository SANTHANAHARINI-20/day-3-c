1.Write a C program that uses a function to determine whether a given positive integer is prime.

#include <stdio.h>

int isPrime(int n) { int i; if (n < 2) return 0; for (i = 2; i * i <= n; i++) { if (n % i == 0) return 0; } return 1; }

int main() { int n; printf("Enter a positive integer: "); scanf("%d", &n);

if (isPrime(n)) printf("%d is a prime number\n", n); else printf("%d is not a prime number\n", n); return 0; } output: Enter a positive integer: 29 29 is a prime number

2.Count a digit using recursion
#include <stdio.h>

int countDigit(int n, int d) { if (n == 0) return 0; if (n % 10 == d) return 1 + countDigit(n / 10, d); return countDigit(n / 10, d); }

int main() { int n, d; printf("Enter a positive integer: "); scanf("%d", &n); printf("Enter the digit to count: "); scanf("%d", &d);

printf("Digit %d occurs %d time(s) in %d\n", d, countDigit(n, d), n); return 0; }

3.Reverse digits using recursion #include <stdio.h>
int reverse(int n, int rev) { if (n == 0) return rev; return reverse(n / 10, rev * 10 + n % 10); }

int main() { int n; printf("Enter a positive integer: "); scanf("%d", &n); printf("Reversed number: %d\n", reverse(n, 0)); return 0; } output: Enter a positive integer: 12345 Reversed number: 54321
