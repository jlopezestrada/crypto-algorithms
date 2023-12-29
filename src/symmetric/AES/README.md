# Advanced Encryption Standard (AES)
The Advanced Encryption Standard, commonly known as AES, represents a pivotal development in the realm of symmetric encryption algorithms. This standard has become an integral part of cryptographic security across the globe, playing a crucial role in a myriad of applications. From securing wireless networks to encrypting files and protecting sensitive data during transit and storage.

## Origins and Development
The story of AES began in 1997 when the National Institute of Standards and Technology (NIST) recognized the need for a more robust encryption standard. The existing Data Encryption Standard (DES), once a stalwart of cryptographic security, was showing its age, especially due to its increasingly vulnerable short key length. NIST was propelled to initiate a global search for a successor that could uphold the growing security needs of the digital age.

The criteria set forth for this new encryption standard were precise and demanding. The proposed solution had to be a symmetric block cipher capable of handling a block size of 128 bits. Moreover, it needed to support multiple key lengths – specifically, 128, 192, and 256 bits – to offer varying levels of security.

This call to action ignited an international response, with cryptographers from around the world throwing their hats into the ring. An initial pool of fifteen algorithms was presented, from which five outstanding candidates emerged: MARS, RC6, Rijndael, Serpent, and Twofish. Each algorithm was rigorously evaluated against a set of criteria that included not just security, but also performance, efficiency, implementability, and flexibility.

The selection process culminated in a significant milestone in the year 2000 when the Rijndael algorithm was chosen. Developed by Belgian cryptographers Vincent Rijmen and Joan Daemen, Rijndael distinguished itself through an optimal blend of security and efficiency, coupled with remarkable performance and flexibility. This winning combination led to its formal adoption by NIST in 2001, when it was officially christened as FIPS PUB 197, marking the birth of what we now know as AES.

## Key Characteristics
Key Characteristics
- **Block Size**: AES operates on 128-bit blocks of data, regardless of the key length.
- **Key Sizes**: It supports key sizes of 128, 192, or 256 bits.
- **Symmetric Key**: The same key is used for both encryption and decryption.

## Encryption Process
Enctyption in AES involves several rounds of processing, depending on the key size: 10 rounds for 128-bit keys, 12 rounds for 192-bit keys, and 14 rounds for 256-bit keys.

1. Initial Round: One step.
- Key Additon: The plaintext is combined with initial key. Each bit of the plaintext is processed using a XOR operation with the corresponding bit of the key.
2. Main Rounds: Four steps.
- SubBytes: Non-linear substitution step where each byte of the block is replaced with another byte according to a predefined lookup table called S-box. S-box, or Substitution box, is a fundamental component in many symmetric key cryptographic algorithms. In the context of AES (Advanced Encryption Standard), it transforms each byte of the block independently, crucial for introducing confusion and thwarting cryptanalysis. See references for more information about S-box.
- ShiftRows: In this step, the rows of the block are cyclically shifted. The first row is not shifted, the second row is shifted one byte to the left, the third row two bytes, and the fourth row three bytes. 
- MixColumns: This transformation mixes the bytes within each column. It treats each column as a four-term polynomial, and these are multiplied modulo a fixed polynomial to produce new columns.
- AddRoundKey: The block is then combined with a round key derived from the original AES key using the key schedule.
3. Final Round: Three steps. Similar to the main rounds but omits the MixColumns step. 
- SubBytes
- ShiftRows
- AddRoundKey

## Decryption Process
Decryption is essentially the reverse of the encryption process, involving the inverse of each step:


## Advanced Encryption Standard (AES) References

### National Institute of Standards and Technology (NIST) Publications
- **NIST's official documentation and publications**: Primary sources for information about AES. 
  - **Key Publication**: FIPS PUB 197, the official document specifying the AES algorithm.
  - **Website**: [NIST.gov](https://www.nist.gov)

### Cryptographic Textbooks and Academic Journals
- **Textbooks on Cryptography**: Such as "Applied Cryptography" by Bruce Schneier, covering the development and technical aspects of AES.
- **Academic Journals**: Research papers and articles for in-depth analysis and historical context.

### IEEE Xplore Digital Library
- **Technical Literature**: Contains literature in engineering and technology, a resource for research papers and articles on AES.
  - **Website**: [IEEE Xplore](https://ieeexplore.ieee.org)

### Cryptographic Conferences and Symposiums
- **Conference Proceedings**: Papers from conferences like Crypto and Eurocrypt discussing the development and analysis of cryptographic algorithms like AES.
