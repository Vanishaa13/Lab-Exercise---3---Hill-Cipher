# Lab-Exercise---3---Hill-Cipher
# AIM

To develop a simple C program to implement Hill Cipher.


# ALGORITHM

1.Start the program.



2.Define the key matrix as a 2 × 2 matrix.



3.Get the plaintext from the user.



4.Convert the plaintext into uppercase and remove spaces.



5.If the plaintext length is odd, add X at the end.



6.Convert each pair of letters into numerical values (A = 0, B = 1, ..., Z = 25).



7.Multiply each pair with the key matrix.



8.Apply modulo 26 to get the encrypted values.



9.Convert the encrypted values into corresponding alphabets.



10.Display the plaintext and ciphertext.



11.Stop the program.


# PROGRAM

```

# Hill Cipher Encryption Program

key = [[3, 3],
       [2, 5]]

plaintext = input("Enter plaintext: ").upper().replace(" ", "")

# Add X if the plaintext length is odd
if len(plaintext) % 2 != 0:
    plaintext += "X"

ciphertext = ""

for i in range(0, len(plaintext), 2):
    a = ord(plaintext[i]) - ord('A')
    b = ord(plaintext[i + 1]) - ord('A')

    c1 = (3 * a + 3 * b) % 26
    c2 = (2 * a + 5 * b) % 26

    ciphertext += chr(c1 + ord('A'))
    ciphertext += chr(c2 + ord('A'))

print("Plaintext:", plaintext)
print("Ciphertext:", ciphertext)

```

# OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0647c0c9-2e9e-4dce-98e1-4deea6ce1943" />



# RESULT

The Hill Cipher program is executed successfully.
