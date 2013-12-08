1. 

```c
#include <stdio.h>
int main()
{
    int M, suma, i;
    suma = 0;
    i = 0;
    printf("Podaj liczbe M: ");
    scanf("%d", &M);
    while (suma < M) {
        i++;
        suma = suma + i;
    }
    printf("Szukane n to: %d\n", i);
    return 0;
}
```

2. 

```c
#include<stdio.h>

int main()
{

    int n, i, count = 0, jest_pierwsza;
    printf("Podaj liczbe calkowita: ");
    scanf("%d", &n);
    for (i = 2; i <= n / 2; i++) {
        if (n % i == 0) {
         count++;
         break;
        }
    }
    if (count == 0 && n != 1)
        jest_pierwsza = 1;
    else
        jest_pierwsza = 0;

    printf("Podana liczba '%d' jest %s\n",
         n, jest_pierwsza ? "pierwsza" : "złożona");
    return 0;
}

```

3. 
```c
#include <stdio.h>
#include <math.h>


long double funkcja_pi(int p)
{
    int i, j;
    long double pi, znak;

    pi = 0;
    znak = 1;

    for (i = 1, j = 0; j < p; j++, i += 2) {
        pi += (znak * 4) / i;
        znak *= (-1);
    }
    return pi;
}

int main()
{

    int liczba;
    printf("Podaj liczbe powtorzen: ");
    scanf("%d", &liczba);

    printf("%d: %.10Lf\n", liczba, funkcja_pi(liczba));
    printf("10: %.0Lf\n", funkcja_pi(10));
    printf("100: %.1Lf\n", funkcja_pi(100));
    printf("1000: %.2Lf\n", funkcja_pi(1000));
    printf("10_000: %.3Lf\n", funkcja_pi(10000));
    printf("100_000: %.4Lf\n", funkcja_pi(100000));
    printf("1_000_000: %.5Lf\n", funkcja_pi(1000000));
    return 0;
}

```

4. 

```c
#include <stdio.h>
int main()
{
   /** deklaracje zmiennych lokalnych */
    int nb, nt, nl, c;
    nb = 0;                        /* liczba znaków odstępu */
    nt = 0;                        /* liczba znaków tabulacji */
    nl = 0;                        /* liczba znaków nowego wiersza */
    while ((c = getchar()) != EOF) {
        if (c == '\n')
         ++nl;
        else if (c == '\t')
         ++nt;
        else if (c == ' ')
         ++nb;
    }
    printf
        ("liczba znaków odstępu = %d, tabulacji = %d, nowego wiersza = %d\n",
         nb, nt, nl);
    return 0;
}

```
