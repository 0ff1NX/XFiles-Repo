# Cryptography

Cryptography is the art of securing digital information by transforming it into an unreadable form, known as ciphertext.

The goal of cryptography is to ensure the CIA, confidentiality, integrity, and authenticity of data transmitted or stored in computer systems.&#x20;



Encryption: the process of converting plaintext into ciphertext using an encryption algorithm and a secret key.

Decryption: converting cipher text to plaintext.



Symmetric

Symmetric: (same): Shared-Key. AES, DES, 3DES.

In symmetric cryptography, the **same** key is used for both encryption and decryption, while in asymmetric cryptography, different keys are used for encryption and decryption.

By using the same key for encryption and decryption, symmetric cryptography ensures that **only parties with the key** can decrypt and access the original data.

Key length refers to the size of the encryption key used in symmetric cryptography, typically measured in bits.

Symmetric cryptography alone does **not** provide data integrity or authentication. Additional mechanisms such as message authentication codes (MACs) or digital signatures are required.



Asymmetric

Asymmetric: public-key. Uses a pair of related keys. A public and private key. The public-key is shared. Elliptic Curve Cryptography (ECC), Rivest-Shamir-Adleman (RSA).





Cryptanalysis is the study of cryptographic systems with the aim of finding weaknesses or vulnerabilities that can be exploited to break or bypass their security.

Perfect forward secrecy (PFS) ensures that the compromise of long-term encryption keys does not compromise the confidentiality of past communications.

A digital signature is used to verify the authenticity and integrity of a digital message or document, ensuring that it has not been altered since it was signed.



There are many reasons on why cryptography is important and are employed into our daily lives that a lot of you are already using.

Some of these might be: One Time Password (OTP)



Some legal information:

Which of the following pieces of legislation defines how HMRC handles a disclosure request?

Freedom of Information Act



Regulation of Investigatory Powers Act

Designed to regulate the powers of public bodies to carry out surveillance of individuals suspected of undertaking fraudulent transactions.



key derivation function (or KDF) derives one or more secret keys from a secret value such as a master key, or known information — such as a password or passphrase — using a pseudo-random function.



symmetrical block cipher that addresses the issues with DES?

AES



Kerckhoff’s

The principle holds that a cryptosystem should be secure, even if everything about the system, except the key, is public knowledge.
