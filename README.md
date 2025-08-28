# File Encrypter/Decrypter

## Overview
This project is a file encryption and decryption tool. It allows users to encrypt or decrypt files in a specified directory using a simple command-line interface.

## Features
- **File Encryption/Decryption**: Encrypts or decrypts files using a key stored in an environment file.
- **Task Management**: Manages tasks for encryption and decryption using a queue system.
- **Process Management**: Handles tasks efficiently with process management.

## Project Structure
```
File_Encrypter_Decrypter/
├── main.cpp                # Entry point of the application
├── src/
│   ├── app/
│   │   ├── encryptDecrypt/
│   │   │   ├── Cryption.cpp
│   │   │   ├── Cryption.hpp
│   │   │   ├── CryptionMain.cpp
│   │   ├── fileHandling/
│   │   │   ├── IO.cpp
│   │   │   ├── IO.hpp
│   │   │   ├── ReadEnv.cpp
│   │   ├── processes/
│   │       ├── ProcessManagement.cpp
│   │       ├── ProcessManagement.hpp
│   │       ├── Task.hpp
├── test/                   # Test files
│   ├── test1.txt
├── .env                    # Environment variables
├── .gitignore              # Git ignore file
├── Makefile                # Build configuration
```

## File Descriptions
### `main.cpp`
The main entry point of the application. It takes user input for the directory path and action (encrypt/decrypt) and processes the files accordingly.

### `Cryption.cpp` and `Cryption.hpp`
Contains the logic for encrypting and decrypting files.

### `CryptionMain.cpp`
A standalone program to execute encryption or decryption tasks.

### `IO.cpp` and `IO.hpp`
Handles file input/output operations.

### `ReadEnv.cpp`
Reads the encryption key from the `.env` file.

### `ProcessManagement.cpp` and `ProcessManagement.hpp`
Manages the queue of tasks and executes them.

### `Task.hpp`
Defines the `Task` structure for managing encryption/decryption tasks.

## How to Build
1. Ensure you have `make` installed.
2. Run the following command to build the project:
   ```bash
   make
   ```

## How to Run
1. After building, run the application:
   ```bash
   ./encrypt_decrypt
   ```
2. Follow the prompts to specify the directory and action.

## Environment Variables
The `.env` file should contain the encryption key. Example:
```
1234
```

## Dependencies
- C++17 or later
- Standard libraries

