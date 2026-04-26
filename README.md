## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
## NAME : SANTHOSH S
## REG NO : 212224100052

## AIM:

To implement the simple substitution technique named Caesar cipher using C Language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:


<img width="741" height="340" alt="img1" src="https://github.com/user-attachments/assets/dae46e46-d6b4-4331-ad57-359a63c951c7" />



## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-
```c
#include <stdio.h>  
#include <string.h>  
#include <ctype.h>  
void main()  
{  
    char plain[10],cipher[10];  
    int key,i,length;      
    int result;      
    printf("\n Enter the plain text:");      
    scanf("%s", plain);      
    printf("\n Enter the key value:");      
    scanf("%d", &key);      
    printf("\n \n \t PLAIN TEXt: %s", plain);      
    printf("\n \n \t ENCRYPTED TEXT:");      
    for(i=0, length = strlen(plain); i<length; i++)  
    {  
        cipher[i]=plain[i] + key;          
        if (isupper(plain[i]) && (cipher[i] > 'Z'))
            cipher[i] = cipher[i] - 26;          
        if (islower(plain[i]) && (cipher[i] > 'z'))
            cipher[i] = cipher[i] - 26;          
        printf("%c", cipher[i]);  
    }  
    printf("\n \n \t AFTER DECRYPTION : ");      
    for(i=0;i<length;i++)  
    {  
        plain[i]=cipher[i]-key;          
        if(isupper(cipher[i])&&(plain[i]<'A'))          
        plain[i]=plain[i]+26;          
        if(islower(cipher[i])&&(plain[i]<'a'))          
        plain[i]=plain[i]+26;          
        printf("%c",plain[i]);  
    }  
} 

```


## OUTPUT :-

<img width="437" height="208" alt="Screenshot 2026-04-25 115135" src="https://github.com/user-attachments/assets/1c96e92e-be3a-4b12-8394-5694402fde0f" />


## Result:
The implementation of the simple substitution technique named Caesar cipher using C language was completed and executed successfully.
