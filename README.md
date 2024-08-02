# Multi-level Post-Quantum Encryption and Lattice Signatures

This Python code demonstrates a combination of 2D-Discrete Wavelet Transform (2D-DWT) with post-quantum cryptographic techniques, including a simulated version of the Falcon signature algorithm, for securing images.

## Motivating Articles and Related Work

Dam, D. T., Tran, T. H., Hoang, V. P., Pham, C. K., & Hoang, T. T. (2023). A survey of post-quantum cryptography: Start of a new race. Cryptography, 7(3), 40.
https://www.mdpi.com/2410-387X/7/3/40

R. Bavdekar, E. Jayant Chopde, A. Agrawal, A. Bhatia and K. Tiwari, "Post Quantum Cryptography: A Review of Techniques, Challenges and Standardizations," 2023 International Conference on Information Networking (ICOIN), Bangkok, Thailand, 2023, pp. 146-151, doi: 10.1109/ICOIN56518.2023.10048976.

Post-quantum Cryptography 
https://openquantumsafe.org/post-quantum-crypto.html

Post-quantum Cryptography NIST 
https://csrc.nist.gov/projects/post-quantum-cryptography

IETF Crypto Forum (cfrg) 
https://datatracker.ietf.org/rg/cfrg/about/

## Results
![](https://github.com/ericyoc/encrypt_aes_keys_with_lattice_sig_poc/blob/main/results_image_series.jpg)

![](https://github.com/ericyoc/encrypt_aes_keys_with_lattice_sig_poc/blob/main/results_table.jpg)

## Key Functionality

1. **2D-DWT**: The code implements both standard and enhanced 2D-DWT to transform the input image.
2. **AES Encryption**: The transformed image coefficients are encrypted using AES encryption.
3. **LWE Encryption**: The AES ciphertext is further encrypted using a simplified version of the Learning With Errors (LWE) post-quantum lattice-based encryption scheme.
4. **Falcon Signing**: A simulated version of the Falcon post-quantum lattice-based signature scheme is used to sign the ciphertext.
5. **Decryption and Verification**: The process is reversed to decrypt the image and verify the Falcon signature.

## Key Concepts and Potential

1. **2D-DWT for Image Transformation**:
   - The standard and enhanced 2D-DWT techniques are used to transform the input images, decomposing them into different frequency bands.
   - This allows for efficient data representation and processing, which is important for secure image processing applications.

2. **AES Encryption for Initial Security**:
   - The transformed image coefficients are encrypted using the AES symmetric-key encryption algorithm.
   - AES provides a high level of security for the image data, ensuring confidentiality.

3. **LWE Encryption for Post-Quantum Security**:
   - The AES ciphertext is further encrypted using a simplified version of the Learning With Errors (LWE) post-quantum lattice-based encryption scheme.
   - LWE is believed to be resistant to attacks by quantum computers, providing an additional layer of security for the image data.

4. **Falcon Signing for Authenticity and Integrity**:
   - A simulated version of the Falcon post-quantum lattice-based signature scheme is used to sign the ciphertext.
   - Falcon's post-quantum properties help ensure the authenticity and integrity of the encrypted image data, preventing unauthorized modifications.

5. **Multi-level Approach for Enhanced Security**:
   - The code demonstrates a multi-level approach by combining the different techniques (2D-DWT, AES, LWE, and Falcon) in a complementary manner.
   - This multi-level approach enhances the overall security of the image processing pipeline, providing confidentiality, integrity, and resistance to quantum computing attacks.

By integrating these techniques, the code showcases the potential of leveraging 2D-DWT in conjunction with post-quantum cryptographic methods to strengthen the security of image processing applications, particularly in domains where sensitive or critical data, such as agricultural images, need to be protected.

The combination of image transformation, symmetric-key encryption, post-quantum encryption, and post-quantum signatures demonstrates a comprehensive security framework that can be further explored and adapted for real-world image processing use cases that require robust protection against both classical and quantum computing-based threats.

## Limitations and Considerations

- The Falcon signature implementation in the code is a simplified simulation and does not represent a true implementation of the algorithm.
- The code is a proof of concept and may not be suitable for production use without further optimization and security auditing.
- The performance and resource requirements of the combined techniques should be carefully evaluated for real-world image processing applications.

This project demonstrates the potential of combining 2D-DWT with post-quantum cryptographic techniques to enhance the security of agricultural image processing applications, ensuring the confidentiality and integrity of sensitive agricultural data.

## Disclaimer
The Python code is for educational and research purposes only.
