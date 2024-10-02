# Encryption Techniques  
What is encryption?   
Encryption is a process that converts plain text (readable data) into a coded format (cipher text) so that only authorized users can read it.  

How It Works:  
1. **Plain Text**: This is the original readable data (like a message or a file).  

2. **Encryption**: A special algorithm (or method) scrambles the plain text into an unreadable format using a key (a secret password or code).  

3. **Cipher Text**: This is the scrambled version of the plain text. It looks like random data and is unreadable without the key.  

4. **Decryption**: To read the original data again, the recipient uses the same key to turn the cipher text back into plain text.  
  
What is the need of encryption:  
Keeps sensitive information safe from unauthorized access (like passwords, personal data, or credit card numbers).  
  
Which algorithm is used?  
AES, AES is a symmetric key algorithm, meaning the same key is used for both encryption and decryption. Both the sender and receiver must keep the key secret.  

AES supports three key lengths: 128 bits, 192 bits, and 256 bits. Longer keys generally provide stronger security but may require more processing power.Modes of Operation:
AES can be used in various modes, each serving different purposes:  

**ECB (Electronic Codebook)**: Simplest mode, where each block is encrypted independently. However, it is not secure for most applications because identical plaintext blocks result in identical ciphertext blocks.  

**CBC (Cipher Block Chaining)**: Each block of plaintext is XORed with the previous ciphertext block before being encrypted, making it more secure than ECB.  
CBC (Cipher Block Chaining) is a mode of operation for block ciphers like AES (Advanced Encryption Standard). It defines how encryption should be performed on blocks of data, ensuring security through the use of an initialization vector (IV) and chaining.  

How CBC works:  

**Splitting into Blocks**:
CBC divides the plain text into fixed-size blocks (e.g., 16 bytes for AES). 
If the data isn’t a multiple of the block size, padding is added to make it fit.
**Initialization Vector (IV)**:
Before encryption, CBC requires an IV (Initialization Vector), which is a random, unique value used for the first block. The IV ensures that even if the same message is encrypted multiple times with the same key, the resulting cipher text will be different.  

**Chaining Process**:
For the first block, the plain text is XORed (combined bit-by-bit) with the IV before encryption.
For the subsequent blocks, the output from the previous block’s cipher text is XORed with the next block of plain text before encrypting.
This creates a "chaining" effect where each block's encryption depends on the previous block's result, making the whole process more secure.  

**Decryption**:
During decryption, each block of cipher text is decrypted and then XORed with the previous block of cipher text (or the IV for the first block) to recover the original plain text. 
  
  Documentation: https://docs.google.com/document/d/1BX8PeZXur9GYPRvwGi99-Cr9NSB-StDDkjjK5-jcXrk/edit?usp=sharing  
    
Glimpse of code work:  
![code](https://github.com/Vidya-coder/Marvel-L2/blob/main/Screenshot%202024-10-02%20050525.png?raw=true)    

![code 1](https://github.com/Vidya-coder/Marvel-L2/blob/main/Screenshot%202024-10-02%20050559.png?raw=true)    

![result](https://github.com/Vidya-coder/Marvel-L2/blob/main/Screenshot%202024-10-02%20050500.png?raw=true)




