# CSpawn Virus

# Enhancement of CSpawn Virus with Data Encryption

The CSpawn Virus, as presented in "The Giant Black Book of Computer Viruses" by Mark Ludwig, serves as an illustrative example of a companion virus. This repository contains an enhanced version of the CSpawn virus that integrates encryption mechanisms to secure both the password and the hostname before writing them to disk. Once encrypted, the virus ensures the decryption of this data in memory when needed, offering a more covert operation.

## Key Modifications:

1. **Encryption Routine:**
   - A new subroutine named `addv` is introduced.
   - Utilizes a basic XOR operation for encryption or decryption of a given string in memory.
   - The chosen encryption key is '3' for this purpose.

2. **Encryption Application:**
   - The encryption is applied on `REAL_NAME` (which represents the hostname) at two main junctions:
     - Before the host execution.
     - Before renaming the original file.

3. **Decryption in Memory:**
   - Before the encrypted data is put to use, the virus ensures it's decrypted back to its original form in memory, making use of the same `addv` subroutine.

## Note:
Remember, the purpose of this exercise is purely educational and should be executed only within a controlled environment. Misuse of this code or its principles outside of these bounds can result in severe consequences, both legally and ethically.

