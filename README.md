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
import java.util.Scanner;

public class CaesarCipher {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

    
        System.out.print("Enter the plain text: ");
        String plainText = sc.nextLine();


        System.out.print("Enter the key value: ");
        int key = sc.nextInt();

        StringBuilder cipherText = new StringBuilder();

  
        for (int i = 0; i < plainText.length(); i++) {
            char ch = plainText.charAt(i);

            if (Character.isLetter(ch)) {
                char base = Character.isUpperCase(ch) ? 'A' : 'a';
            
                char newChar = (char) ((ch - base + key) % 26 + base);

        
                if (newChar < base) {
                    newChar += 26;
                }

                cipherText.append(newChar);
            } else {
           
                cipherText.append(ch);
            }
        }

  
        System.out.println("Cipher Text: " + cipherText.toString());

        sc.close();
    }
}

```

## OUTPUT:

<img width="705" height="398" alt="image" src="https://github.com/user-attachments/assets/976b19ab-a86c-4aed-a207-9511a42a9975" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
