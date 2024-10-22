# Implement-DES-Encryption-and-Decryption
## AIM
To encrypt and decrypt the given message using the DES (Data Encryption Standard) algorithm.
## ALGORITHM :
Step 1:
Design of the DES algorithm.

Step 2:
Implementation using C or Python code.

Step 3:
The DES algorithm takes a 64-bit block of plaintext and a 56-bit key to perform encryption through a series of transformations, including permutation, substitution, and XOR operations.

Step 4:
The encryption process involves 16 rounds of these transformations.

Step 5:
The decryption process reverses the steps to retrieve the original message.

## PROGRAM :
```
#include <stdio.h>
#include <string.h>

void simpleEncrypt(char *plaintext, char key, char *ciphertext)
{
    for (int i = 0; plaintext[i] != '\0'; i++) 
    {
        ciphertext[i] = plaintext[i] ^ key; 
    }
    ciphertext[strlen(plaintext)] = '\0'; 
}

void simpleDecrypt(char *ciphertext, char key, char *decryptedText) {
    for (int i = 0; ciphertext[i] != '\0'; i++) 
    {
        decryptedText[i] = ciphertext[i] ^ key; 
    }
    decryptedText[strlen(ciphertext)] = '\0'; 
}

int main() {
    char plaintext[100], ciphertext[100], decryptedText[100];
    char key;
    printf("Enter the plaintext: ");
    scanf("%s", plaintext);
    
    printf("Enter a key (a single character): ");
    scanf(" %c", &key);
    
    simpleEncrypt(plaintext, key, ciphertext);
    printf("Encrypted Message (ASCII values): ");
    
    for (int i = 0; ciphertext[i] != '\0'; i++) {
        printf("%d ", (unsigned char)ciphertext[i]);
    }
    printf("\n");
    
    simpleDecrypt(ciphertext, key, decryptedText);
    printf("Decrypted Message: %s\n", decryptedText);

    return 0;
}
```
## OUTPUT:

![Screenshot 2024-10-13 161718](https://github.com/user-attachments/assets/10d14bbc-37a8-488b-97de-01ebeb8e923f)

## RESULT:
The program for DES algorithm is executed successfully.
