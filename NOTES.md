# QxQ-Quantum-Computing-Capstone-Projects

## Description
This repository contains capstone projects related to Quantum Computing, specifically focusing on quantum encryption techniques such as BB84 protocol.

## Tech Stack
- Python (for implementing the BB84 protocol and AES encryption)
- Jupyter Notebooks (for data analysis and experimentation)

## Usage
The repository includes a single Jupyter Notebook file: `BB84_Eves_Intercept_and_Resend_Attack_AES256.ipynb`. This notebook contains code for simulating an eavesdropping attack using the BB84 protocol in conjunction with AES encryption. The project also discusses the importance of robust encryption and security measures, particularly in a quantum computing environment.

### Contents
- `BB84_Eves_Intercept_and_Resend_Attack_AES256.ipynb`: Contains Python code for simulating an eavesdropping attack using the BB84 protocol with AES encryption. 

## Analysis
The project highlights the importance of strong encryption and meticulous verification processes to ensure data security in a quantum computing context. It also underscores the need for robust security measures, such as quantum key distribution (QKD), to detect and prevent interception attempts.

### Key Points
- **BB84 Protocol**: A method used to observe eavesdropping activities by monitoring anomalies in the quantum bit error rate (QBER).
- **AES Encryption**: Used due to its balance of security, efficiency, and flexibility.
- **Intercept and Resend Attack Strategy**: Implemented to detect potential eavesdroppers based on QBER changes.
- **Security Measures**: Emphasizes the importance of using robust encryption algorithms, proper key management, regular audits, user training, and post-quantum cryptography.

## Conclusion
The development of quantum encryption is crucial for securing future communications against emerging threats from quantum computing. Traditional cryptographic systems are vulnerable to quantum computers' potential to break them easily, whereas quantum encryption leverages principles like entanglement and superposition to create uncrackable encryption methods that ensure the confidentiality and integrity of transmitted data.

As the digital landscape evolves and the risk of quantum attacks increases, the advancement of quantum encryption technologies is not only important but essential for safeguarding sensitive information across various sectors.


# QxQ-Quantum-Computing-Capstone-Projects

INTRODUCTION 

In the development of this encryption project in Python, the selection of a robust and efficient encryption algorithm was prioritized. Initially, the Vernam Cipher was experimented with, but its application proved impractical for large texts due to the excessive size of the resulting cipher. For this reason, AES encryption was chosen, which allows variable length keys (16, 24 or 32 bytes), taking advantage of the flexibility and security it offers. 
 
The final decision to use AES was based on its balance of security, efficiency, and flexibility, as well as its wide adoption and support in the cybersecurity community. These factors were crucial to ensure robust data protection and operational practicality within the scope of the encryption project. The choice of the Python cryptography library was based on its compatibility with the most recent version of Python, thus ensuring continuous update and support. 

Choosing the Intercept and Resend Attack strategy in the context of the BB84 protocol is an astute decision to observe the activities of a potential eavesdropper like Eve. This method is based on the premise that any eavesdropping attempt on a quantum channel, such as qubit interception and forwarding, introduces detectable anomalies in the quantum bit error rate (QBER). Therefore, by monitoring the QBER, the presence of an eavesdropper can be inferred. The BB84 protocol is resistant to these types of attacks due to its quantum structure, which guarantees that any perturbation in the quantum states of the qubits will be evident to the legitimate participants, Alice and Bob. Furthermore, recent studies have analyzed the effect of a depolarizing channel on the security of the BB84 quantum key distribution, finding that the quantum error rate decreases with increasing the depolarization parameter, which characterizes the channel noise. These investigations are fundamental to understanding and improving security in quantum communication, ensuring that information remains protected even in the presence of interception and forwarding attempts by third parties. 
 
Implementing encryption presented significant technical challenges. One of them was the need to convert the Final Key from a binary format to a base64 string, which was achieved using the base64 library. In addition, it had to be ensured that the length of the Final Key met the requirements of AES encryption, for which a function was developed that adjusts the length of the key by adding an additional byte if necessary. 
 
The key verification process involved two critical stages: first, a partial check of Alice and Bob's keys to confirm their correspondence; the second, a complete verification of bases and keys between Alice and Bob. This two-phase approach ensured the integrity of the encryption and non-interference from third parties. Finally, the bases and bits shared by Alice and Bob were verified to derive the final keys, ensuring that both parties operated under the same cryptographic conditions. This project not only highlights the importance of strong encryption but also the meticulousness required in verifying and validating information security. 

ANALYSIS 

The presence of a spy in the data encryption and decryption process can have significant consequences. In a symmetric encryption scenario, if an eavesdropper manages to obtain the secret key, he or she could decrypt any message encrypted with that key, compromising the confidentiality of the information. In the case of asymmetric encryption, even if the spy has access to the public key, he will not be able to decrypt the data without the corresponding private key. However, if you manage to access the private key, the security of the data is equally compromised. Additionally, an active eavesdropper could alter messages during transmission, which might go undetected without integrity mechanisms such as digital signatures or message authentication codes. On the other hand, in a quantum cryptography system like the BB84 protocol, the interception and forwarding of qubits by an eavesdropper would increase the quantum bit error rate (QBER), alerting legitimate users to the presence of a suspicious activity. Therefore, it is crucial to implement robust security measures, such as quantum key distribution (QKD), that detect the presence of eavesdroppers and protect the integrity and confidentiality of transmitted data. 

To mitigate the impact of an eavesdropper on cryptographic systems, it is essential to take a multifaceted approach that includes both technical and procedural measures. Technically, implementing robust encryption algorithms and proper key management are essential. This involves using algorithms that have been widely reviewed and accepted by the security community, as well as ensuring that keys are long and complex enough to withstand brute force attacks. Additionally, regular key rotation and the use of ephemeral keys can prevent long-term access to encrypted data even if a key is compromised. Procedurally, it is crucial to conduct periodic security audits, train users in good security practices, and establish clear policies for handling sensitive information. Post-quantum cryptography is also emerging as a long-term solution to protect against threats posed by quantum computers. Finally, implementing transport layer security protocols, such as TLS, can help secure communications in transit and prevent man-in-the-middle attacks. In summary, effective mitigation requires a defense-in-depth strategy that addresses both the strength of cryptographic algorithms and the policies and practices surrounding their use. 

CONCLUSION 

The evolution of quantum cryptography is crucial to the future of secure communications due to its ability to protect against emerging threats from quantum computing. As quantum computers become more powerful, classical encryption algorithms risk becoming obsolete, since a quantum computer could, in theory, break them relatively easily. Quantum cryptography, on the other hand, uses the properties of quantum mechanics, such as entanglement and superposition, to create encryption systems that cannot be cracked by quantum computers, thus ensuring the confidentiality and integrity of the transmitted information. Furthermore, the uncertainty principle and eavesdropping detection inherent to quantum cryptography offer a level of security that is fundamentally unattainable with traditional encryption methods. Therefore, the development of quantum cryptography is not only important, but essential to safeguard the privacy and security of communications in the near and distant future. 
 
The development of quantum encryption is pivotal for the future of secure communication because it offers a solution to the vulnerabilities presented by the advent of quantum computing. Traditional cryptographic systems rely on the computational difficulty of certain mathematical problems, which quantum computers are expected to solve with ease, rendering current encryption methods ineffective. Quantum encryption, however, leverages the principles of quantum mechanics, such as entanglement and the non-cloning theorem, to create encryption that cannot be cracked by quantum computers, ensuring the confidentiality and integrity of data. 

Moreover, quantum encryption protocols like Quantum Key Distribution (QKD) provide a means of detecting any interception attempts, as the act of measuring a quantum system inevitably alters its state. This feature enables two parties to communicate with the assurance that their encryption keys remain private, and if compromised, can be promptly invalidated before any data breach occurs. 

As the digital landscape evolves and the potential for quantum attacks becomes more imminent, the development of quantum encryption technologies is not just important but essential. It ensures that our communications infrastructure can withstand future threats, safeguarding sensitive information across various sectors, from national security to personal data privacy. The proactive advancement of quantum encryption is therefore a critical step in preserving the security and trustworthiness of global communications in the post-quantum era. 
