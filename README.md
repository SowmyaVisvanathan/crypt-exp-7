#### Name : Sowmya V
#### Reg no : 212222110045
#### Date : 

## EX - 8 : Implementation of AES

### Aim:
Implementation of Advanced Encryption Standard

### Algorithm

1. Start.


2. Initialize the input URL that you want to encrypt (e.g., "https://example.com/search?q=test").
3. Define a key for encryption (KEY = 0xAA).
4. Calculate the length of the input URL (i.e., the number of characters).
5. Call the encryption function:
  Loop through each character of the input URL.
  Store the result (encrypted value) in the output array.
6. Print the encrypted URL:
  Display the encrypted values as a hexadecimal string.
7. Call the decryption function:
  Loop through each character of the encrypted URL.
  Store the result (decrypted value) in the output array.
8. Print the decrypted URL to verify that it matches the original input URL.
9. End

### Program:
```
#include <stdio.h>
#include <string.h>
#define KEY 0xAA  

void xor_encrypt_decrypt(char *input, char *output, int length) 
{
    for (int i = 0; i < length; i++) 
    {
        output[i] = input[i] ^ KEY;
    }
    output[length] = '\0'; 
}

int main() 
{
    char url[] = "https://example.com/search?q=test";  
    char encrypted[256];  
    char decrypted[256];  
    int length = strlen(url);

    xor_encrypt_decrypt(url, encrypted, length);
    printf("Encrypted URL: ");
    for (int i = 0; i < length; i++) 
    {
        printf("%02x", (unsigned char)encrypted[i]);  // Print in hex format
    }
    printf("\n");
    xor_encrypt_decrypt(encrypted, decrypted, length);
    printf("Decrypted URL: %s\n", decrypted);
    return 0;
}
```
### Output

![image](https://github.com/user-attachments/assets/68fc66a1-f49f-4ec9-8155-dccb3a5d7ef8)

### Result
Implementation of Advanced Encryption Standard to encrypt and decrypt url was successful.
