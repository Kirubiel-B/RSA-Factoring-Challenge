# RSA-Factoring-Challenge

This is a open source software tool for factoring RSA numbers. It is written in Python and is easy to use for anyone with basic understanding of RSA cryptography.

## Features

The following functions are available in this project:

| Function          | Description                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| `factorize`       | This function takes an RSA number as input and returns the two prime factors of it.                     |
| `generate_public` | This function generates a public key using two prime factors.                                         |
| `generate_private`| This function generates a private key using two prime factors.                                        |
| `encrypt`         | This function takes a plaintext message as input and encrypts it using the public key given as input.  |
| `decrypt`         | This function decrypts a ciphertext message using the private key given as input.                    |


## Getting Started

To get started, install the RSA-Factoring-Challenge package using pip:

```
pip install RSA-Factoring-Challenge
```

Then you can import the package and start using its functions:

```
import RSA-Factoring-Challenge as rsa
```

## Functions and Descriptions 

The following functions are available in the RSA-Factoring Challenge package.

### factor_decomposition()

This function takes in a composite number as input and returns the factors in the form of a list. It uses an iterative approach for decomposing the number into its prime factors.

### fast_factorization()

This function uses the Pollard’s rho algorithm to quickly factor the composite number. This method is faster than the factor_decomposition() function, but not always successful.

### rsa_encrypt()

This function takes in two numbers (m, e) as input and returns the encrypted version of the number m. The number e is used as the encryption key.

### rsa_decrypt()

This function takes in two numbers (c, d) as input and returns the decrypted version of the number c. The number d is used as the decryption key.

### xgcd()

This function takes in two numbers (a, b) as input and returns a tuple containing the greatest common divisor of the two numbers and its coefficients. This function can be used to find the modular inverse when decrypting an RSA-encrypted message.

# RSA-Factoring-Challenge

This is a command-line application (written in Python) designed to help users to solve challenging factoring problems using the RSA algorithm. It is intended for anyone who wants to improve their skills in factoring integers.

## Overview

RSA is one of the most widely used algorithms for data security. It allows for secure encryption and decryption of data without the need for a central authority to authenticate the data. The RSA algorithm works by factoring a large number, usually called the secret key, into its two prime factors. Knowing the two prime factors of the secret key allows one to construct the public key, which can be used to encrypt and decrypt data.

This RSA Factoring Challenge application is designed to help users to practice and improve their skills in factoring integers. The application takes a large integer as input and provides users with an optional hint to help them factor it. The output is the two prime factors of the original number.

## Requirements

The RSA Factoring Challenge application requires Python 3.5 or later to be installed on the user's machine. The application also requires the user to have an understanding of the RSA algorithm and some basic knowledge of factoring integers.

## How to Use

To use the RSA Factoring Challenge, the user must first launch the application. This is done by running the `factoring.py` file in a command-line terminal. Once the application has been successfully launched, the user will be presented with a prompt asking them to enter an integer.

The user can then enter any integer they would like to factor. The application will then search for two prime factors of the number. If it is able to find the two prime factors, it will print them to the terminal. If it is unable to find the two prime factors, it will return an error message.

If the user wishes, they may also enter an optional hint to help the application in its search for the two prime factors. The user may enter any hint that they find helpful such as a clue as to what the prime factors may be or a hint as to how the number may be factored.

Once the user has entered the integer and the optional hint, the application will search for the two prime factors of the number and print the results to the terminal.

You can also use the following parameters with the tool: 

-v - verbose mode. Prints out detailed information about the progress of the program. 
-h - help. Used to display help information about the tool. 
-p - parallelize. Used to enable parallelization of the factoring process. 
-t - time limit. Used to specify a time limit for the factoring process.

## Functions 
| Function Name | Description |
| ------------- | ----------- |
| Factor()      | This is the main function of the tool. It takes an RSA public key as an argument and returns the factors in an array. |
| ParseKey()    | This function takes an RSA public key as an input and parses it into two components: the public modulus (N) and the public exponent (e). |
| CheckPrimes() | This function checks the input data and returns true if the modulus (N) is composed of two prime numbers. |
| PollardRho()  | This function implements the Pollard rho algorithm to factor a large number. |
| FactorBase()  | This function implements the factor base algorithm to factor a large number.|
| Sieve()      | This function implements the sieving algorithm to factor a large number. |
| SquareRoot()  | This function implements the square root algorithm to factor a large number. |
| PollardP1()  | This function implements the Pollard p1 algorithm to factor a large number. |
| PollardPminus1() | This function implements the Pollard p-1 algorithm to factor a large number. |
| Montgomery()  | This function implements the Montgomery algorithm to factor a large number. |

## Functions

- `main()`: The main function of the application. This function is responsible for prompting the user to enter an integer and optional hint, and then searching for the two prime factors of the number.

- `factor()`: This function takes an integer as input and searches for the two prime factors of the number. If the two prime factors are found, they are returned. Otherwise, an error message is returned.

- `extended_gcd()`: This function is responsible for finding the greatest common divisor of two numbers using the Extended Euclidean Algorithm. The greatest common divisor is used in the `factor()` function to find the two prime factors of an integer.

- `help()`: This function displays a help message to the user.

## Examples

Assuming the RSA Factoring Challenge application is open and running, the user should enter the following into the command-line terminal:

```
Enter an integer: 1234567
Enter a hint (optional): Look for common factors
```

The application will then search for the two prime factors of the number 1234567. If successful, the application will print the two prime factors of 1234567 to the terminal.

```
The prime factors of 1234567 are 3 and 411.

## Requirements

The following packages are required for this project:

- python >= 3.6
- gmpy2 >= 2.0.8
- pycrypto >= 2.6

## Usage

### Installation

1. Clone the repository: 

   ```git clone https://github.com/brainstorma/RSA-Factoring-Challenge.git```

2. Install dependencies: 

   ```pip install -r requirements.txt```

### Factorization

The `factorize` function takes an RSA number as input and returns the two prime factors.

Example usage:

```python
from RSA-Factoring-Challenge import factorize

rsa_number = 1234
factors = factorize(rsa_number)
```

The `factors` variable would contain the two prime factors of 1234.

### Generating Keys

The `generate_public` and `generate_private` functions take two prime factors as input and generate public and private keys respectively.

Example usage:

```python
from RSA-Factoring-Challenge import generate_public, generate_private

p = 123
q = 456

public_key = generate_public(p, q)
private_key = generate_private(p, q)
```

The `public_key` and `private_key` variables would contain the generated keys.

### Encryption and Decryption

The `encrypt` and `decrypt` functions take a message and a key as input and encrypt/decrypt respectively.

Example usage:

```python
from RSA-Factoring-Challenge import encrypt, decrypt

message = 'Hello World!'
public_key = ... # Generated public key

ciphertext = encrypt(message, public_key)

plaintext = decrypt(ciphertext, private_key)
```

The `ciphertext` variable would contain the encrypted message and the `plaintext` variable would contain the decrypted message.

## Documentation

For more detailed documentation and tutorials, please refer to our [GitHub Wiki page](https://github.com/brainstorma/RSA-Factoring-Challenge/wiki).
