# 🔒 Caesar Cipher

### **Introduction**&#x20;

The Caesar cipher, named after Julius Caesar who is historically attributed to its use, stands as one of the earliest and simplest encryption techniques in the history of cryptography. This substitution cipher, falling under the category of symmetric encryption, involves shifting the letters of the alphabet by a fixed number of positions to secure the content of a message.

### **Historical Significance**

Julius Caesar, the Roman military and political leader, is said to have used this cipher to protect sensitive military communications. The simplicity of the method allowed for quick encryption and decryption by those familiar with the shift value.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>CAESAR cipher with shift of "3"</p></figcaption></figure>

### **Key Principles**

1. **Substitution Method:** The Caesar cipher operates on the principle of letter substitution. Each letter in the plaintext is replaced by a letter a fixed number of positions down or up the alphabet.
2. **Key:** The key in the Caesar cipher is the numerical value representing the shift applied to each letter. For example, with a shift of 3, 'A' would be encrypted as 'D,' 'B' as 'E,' and so forth.

### **Characteristics**

1. **Simplicity:** The Caesar cipher is remarkably simple in its implementation, making it a suitable choice for educational purposes and basic encryption needs.
2. **Vulnerability:** Due to its simplicity, the Caesar cipher is highly vulnerable to brute-force attacks. With only 25 possible shift values (excluding the trivial case of no shift), an attacker could systematically test all combinations to decrypt the message.
3. **Shift Variations:** While the traditional Caesar cipher involves shifting letters in a fixed direction (right or left), variations exist where the shift pattern may change within the message, enhancing security but also complexity.

### **Brute Force Attack**

* **Method:** A brute-force attack on the Caesar cipher involves systematically trying all possible shift values until the correct one is found.
* **Vulnerability:** Given the limited number of shift values, the Caesar cipher is highly susceptible to brute-force attacks, even without advanced computing power.

### CODE

> To access the full version of our code, visit our [**GitHub**](https://github.com/AjaxSX1/CryptoXDEV/blob/main/Caesar%20Cipher/CaesarCipherCracker.py) repository.

#### Importing Libraries:

```python
from termcolor import colored
from time import sleep
```

* The `termcolor` library is imported for adding colored text output to the console.
* The `time` library is imported for introducing a delay using the `sleep` function.

#### Caesar Cipher Functions:

**`decrypt()` Function:**

```python
def decrypt():
    # ... (user input for encrypted_message and key)
    
    for ch in encrypted_message:
        # ... (decryption logic)

    print("Your decrypted message is: ", decrypted_message, end="\n")
    repeat()
```

* This function prompts the user for an encrypted message and a key to decrypt the message.
* It then iterates through each character in the encrypted message, decrypts it using the provided key, and builds the decrypted message.
* Finally, it prints the decrypted message and calls the `repeat()` function to check if the user wants to perform another operation.

**`encrypt()` Function:**

```python
def encrypt():
    # ... (user input for plaintext_message and key)

    for ch in plaintext_message:
        # ... (encryption logic)

    print("Your encrypted message is: ", encrypted_message, end="\n")
    repeat()
```

* Similar to `decrypt()`, this function encrypts a user-provided plaintext message using a key.
* It iterates through each character in the plaintext, encrypts it, and builds the encrypted message.
* The result is printed, and the `repeat()` function is called for further operations.

**`bruteforce()` Function:**

```python
def bruteforce():
    # ... (user input for encrypted_message)

    for key in range(26):
        # ... (brute-force decryption logic)

    repeat()
```

* This function attempts to brute-force decrypt an encrypted message by trying all possible shift values (keys).
* It prints the result of each attempt, showing the decrypted message for each key.

#### Allowed Member IDs:

```python
allowed_ids = ["XDEV-0000", "XDEV-0002", ... "XDEV-0118"]
```

* This list contains allowed member IDs. Access is granted only if the entered member ID is present in this list.

#### Login and Main Program Flow:

```python
def login():
    # ... (user input for member_id)

    if member_id not in allowed_ids:
        print("Access denied. Your member ID is not authorized.")
        login()
    elif member_id in allowed_ids:
        choose()

def choose():
    # ... (user input for choice)

    match choice:
        case 1:
            decrypt()
        case 2:
            encrypt()
        case 3:
            bruteforce()
        case _:
            return

def repeat():
    # ... (user input for continuing)

    if WantToRepeat == "Y":
        choose()
    else:
        return

# Program Entry Point
print(colored("... (ASCII art logo)", "green"))
login()
```

* The program starts with an ASCII art logo printed in green.
* The `login()` function is called, which prompts the user for a member ID. Access is granted only if the ID is in the `allowed_ids` list.
* After successful login, the user is presented with a menu (`choose()`) to perform decryption, encryption, or brute-force decryption.
* The `repeat()` function is used to check if the user wants to continue after completing an operation.

### Application

#### Encryption

* For each letter in the plaintext, a fixed shift is applied.
* The resulting cipher text is then composed of the substituted letters.

**Example:**

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

* **Plain Text:** HELLO
* **Shift:** 3
* **Cipher Text:** KHOOR

#### Decryption

* The process is reversed by shifting each letter in the cipher text in the opposite direction.
* The original plaintext is thus revealed.

**Example:**

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

* **Cipher Text:** KHOOR
* **Shift:** 3 (reverse)
* **Decrypted Text:** HELLO

### **Conclusion**

The Caesar cipher, though antiquated and relatively insecure by modern standards, holds historical importance as a foundational encryption technique. Understanding its principles, vulnerabilities, and susceptibility to brute-force attacks provides insights into the evolution of cryptographic methods and serves as a stepping stone to more advanced encryption technologies.
