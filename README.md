# Cracking-with-JTR

## Overview

This project is designed to familiarize users with password cracking techniques and tools using John the Ripper (JTR). The focus is on cracking bcrypt (Blowfish 32/64 X3) hashed passwords.

## Requirements

- **John the Ripper (JTR):** Ensure you have John the Ripper installed on your system. You can download it from [here](https://www.openwall.com/john/).

## Files

- **`worldlist.txt:`** A wordlist file containing a list of potential passwords used in the cracking process.
- **`password.txt:`** A file containing bcrypt hashed passwords that need to be cracked.

## Getting Started

1. **Install John the Ripper:**

   Follow the installation instructions from the official [John the Ripper website](https://www.openwall.com/john/).

2. **Prepare the Files:**

   Place the `worldlist.txt` and `passwords.txt` files in the same directory as the John the Ripper executable or specify the path to these files in the commands.

3. **Run John the Ripper:**

   Use the following command to start cracking the bcrypt hashes using the provided wordlist:

   ```bash
   john --wordlist=worldlist.txt --format=bcrypt password.txt

  **Command Options**
  
- `--wordlist=worldlist.txt`: Specifies the wordlist file to be used.
- `--format=bcrypt`: Specifies the hash format to crack.
- `password.txt`: The file containing the hashed passwords.

## Check Results

After running John the Ripper, you can view the cracked passwords with the following command:

```bash
john --show password.txt
