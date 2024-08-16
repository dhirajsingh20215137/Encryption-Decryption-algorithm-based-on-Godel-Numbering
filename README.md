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

## Installation

To use this project, clone the repository and compile the code using a C++ compiler. The following steps will guide you through the setup:

```bash
git clone https://github.com/yourusername/GodelNumberingEncryption.git
cd GodelNumberingEncryption

## Encryption and Decryption Process](#encryption-and-decryption-process
     


