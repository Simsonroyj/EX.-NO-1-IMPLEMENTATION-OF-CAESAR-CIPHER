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
def caesar(text, shift, mode):
    result = ""
    if mode == "decrypt":
        shift = -shift

    for char in text:
        if char.isalpha():
            base = 65 if char.isupper() else 97
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char
    return result

text = input("Enter text: ")
shift = int(input("Enter shift value: "))

encrypted = caesar(text, shift, "encrypt")
print("Encrypted:", encrypted)
print("Decrypted:", caesar(encrypted, shift, "decrypt"))
```
## OUTPUT:
<img width="360" height="265" alt="image" src="https://github.com/user-attachments/assets/2fa89a5a-3dcb-48a9-90f0-ed4d58b4352f" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
