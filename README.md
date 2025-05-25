# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm
## Name: KABILAN V
## Reg no: 212222100018

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1.Get the input for prime number p.

2.Calculate the primitive root of p that is g.

3.Calculate private keys for both users using p and g values.

4.Similarly, secret keys for both users are calculated.

## Program:
```
#include <math.h>
#include <stdio.h>

long long int power(long long int a, long long int b, long long int P)
{
    if (b == 1)
        return a;
    else
        return (((long long int)pow(a, b)) % P);
}


int main()
{
    long long int P, G, x, a, y, b, ka, kb;

    printf("\n\t***** Diffie-Hellman Key Exchange Algorithm *****\n\n");

    
    printf("Enter the value of P: ");
    scanf("%lld", &P);
    printf("The value of P: %lld\n", P);

    printf("Enter the value of G (Primitive root of P): ");
    scanf("%lld", &G);
    printf("The value of G: %lld\n\n", G);


    a = 4;
    printf("The private key a for Alice: %lld\n", a);
    x = power(G, a, P); 

  
    b = 3;
    printf("The private key b for Bob: %lld\n\n", b);
    y = power(G, b, P); 


    ka = power(y, a, P); 
    kb = power(x, b, P); 

    printf("Secret key for the Alice is: %lld\n", ka);
    printf("Secret Key for the Bob is: %lld\n", kb);

    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/4bab0c78-f22d-4d77-b4f7-319e9881de13)


## Result:
  The program is executed successfully

