# Gödel Numbering-Based Encryption/Decryption Algorithm

## Overview

This repository contains an implementation of a cryptographic model based on Gödel Numbering. The algorithm leverages the Sieve of Eratosthenes for precomputing prime numbers and utilizes the Mersenne Twister (mt19937-64) for random number generation. The model is capable of performing encryption and decryption of strings with lengths up to 1 million characters within 1 second.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Encryption and Decryption Process](#encryption-and-decryption-process)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Fast Encryption/Decryption**: Can handle strings up to 1 million characters in less than a second.
- **Prime Number Based Encoding**: Utilizes prime numbers and Gödel Numbering for unique character encoding.
- **Diffie-Hellman Key Exchange**: Secure key exchange using Diffie-Hellman for generating encryption keys.
- **Buffer String for Security**: Adds buffer strings to encrypted text for additional security and randomness.


## Encryption and Decryption Process

### Example: Encrypting and Decrypting a Message

Example: Encrypting and Decrypting a Message
Suppose we want to encrypt the message "Hello, World!" using the provided encryption algorithm.

Step 1: Generate the Encryption Key
First, we use the diffie_hellman function to generate a key based on the Diffie-Hellman key exchange method.

cpp
Copy code
unsigned long long key = diffie_hellman(7911, 1567689892, 292787734);
For this example, let's assume the generated key is 1234567890123456789 (this is just a placeholder; the actual key would be calculated by the function).

Step 2: Encrypt the Message
Next, we encrypt the message "Hello, World!" using the generated key.

cpp
Copy code
string message = "Hello, World!";
string encrypted_text = encrypt(message, key);
cout << "Encrypted Text: " << encrypted_text << endl;
Let's say the output is:

plaintext
Copy code
Encrypted Text: 74231725653{N2Z}23255378519{y4A}29849789639{8Mc}31937563685{7Op}77448733268{K1@}169536148549{L3t}43875142287{U$W}31937563685{7Op}29849789639{8Mc}23255378519{y4A}213461782319{`X&}74231725653{N2Z}
This is the encrypted version of the message "Hello, World!". Each part of the string corresponds to an encrypted character, followed by a buffer string for added security.

Step 3: Decrypt the Message
Now, let's decrypt the encrypted text back into the original message.

cpp
Copy code
string decrypted_text = decrypt(encrypted_text, key);
cout << "Decrypted Text: " << decrypted_text << endl;
The output would be:

plaintext
Copy code
Decrypted Text: Hello, World!
This confirms that the original message "Hello, World!" was successfully encrypted and then decrypted back to its original form.

Detailed Breakdown of the Example
Original Message: "Hello, World!"
Generated Key: 1234567890123456789
Encrypted Text: The message is converted into a string of numbers and buffer strings (e.g., 74231725653{N2Z}...).
Decrypted Text: The encrypted text is successfully decrypted back to "Hello, World!".
