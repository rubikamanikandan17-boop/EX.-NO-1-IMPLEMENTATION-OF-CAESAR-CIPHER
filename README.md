# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100] = "Rubikamanikandan";
    char cipher[100];
    int key = 3, i;

    printf("Plain Text: %s\n", text);
    printf("Key: %d\n", key);

    for(i = 0; text[i] != '\0'; i++)
    {
        cipher[i] = (text[i] - 'A' + key) % 26 + 'A';
    }
    cipher[i] = '\0';

    printf("Encrypted Text: %s\n", cipher);

    for(i = 0; cipher[i] != '\0'; i++)
    {
        text[i] = (cipher[i] - 'A' - key + 26) % 26 + 'A';
    }
    text[i] = '\0';

    printf("Decrypted Text: %s\n", text);

    return 0;
}
```

## OUTPUT:
<img width="1601" height="697" alt="Screenshot 2026-10-22 091419" src="https://github.com/user-attachments/assets/f460237e-839e-48c1-8c52-cd7fee5e61fc" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
