# SecureVault: Zero-Knowledge Proofs for Verified Data Access


## Overview
#### Contract address: 0x4aa8863dd0c93793b2925b7f9c72700fbc1e11ac
\- Deployed on Etherlink Blockchain(testnet)
SecureVault is a blockchain-based solution leveraging **Zero-Knowledge Proofs (ZKPs)** for secure and privacy-preserving data verification. The primary focus of the project is to enable third-party applications to access user-specific data fields without compromising their privacy, all while ensuring trust and transparency using blockchain technology.

Our project integrates **IPFS**, **Zokrates**, and **smart contracts** to create a secure system for validating age requirements (as a proof of concept). This foundation can be extended to other fields like education, employment, or financial status.
---
## Demo Videos

- **Data Verification**: [View on Google Drive](https://drive.google.com/drive/folders/1Q4yLtJnJHk_VBONQqyiqAl56xWQqctKj?usp=sharing)
- **Document Upload**: [View on Google Drive](https://drive.google.com/file/d/1QmkNkeKfdkraaHU1BjChahaaBZjJmVy-/view?usp=sharing)
---

## Key Features

- **Zero-Knowledge Proof (ZKP) Integration**  
  Validate specific data fields without revealing complete details (e.g., prove age > 18 without sharing the exact date of birth).

- **Decentralized Storage (IPFS)**  
  Stores encrypted data and allows CID-based access for secure retrieval.

- **Blockchain-Secured Proofs**  
  Proofs generated by Zokrates are validated by smart contracts on the blockchain, ensuring tamper-proof verification.

- **Scalable API Generator** *(Future Vision)*  
  The project aims to evolve into an API generator for third-party applications to verify custom fields (e.g., educational credentials, financial status).

---

## How It Works

1. **Request**: A third-party application (e.g., Instagram) sends a request to SecureVault.  
2. **User Input**: The user provides:
   - A **CID** (Content Identifier) from IPFS.
   - The field they want to verify (e.g., age).  
3. **Data Retrieval**: IPFS decodes the CID and retrieves the required user data.  
4. **Proof Generation**:  
   - The data and verification question are sent to Zokrates, which generates a **zero-knowledge proof**.  
5. **Proof Validation**:  
   - The smart contract validates the proof and records the transaction on the blockchain.  
6. **Access Decision**:  
   - If the proof is valid, access is granted; otherwise, it is denied.  
   - A block is added to the chain indicating the result (agreed/denied).

---

## Current Use Case: Age Verification

Our implementation verifies if the user is above 18 years old, demonstrating the power of ZKPs for privacy-focused identity checks.  

### Fields That Can Be Masked Using ZKPs:
- **Identity Verification**: Prove identity without revealing full details.
- **Citizenship or Residency**: Verify status without disclosing location specifics.
- **Employment Status**: Confirm employment without exposing the company or role.
- **Financial Information**: Validate eligibility for credit without sharing full financial data.
- **Education Credentials**: Prove academic qualifications without revealing full transcripts.

---

## Blockchain Contents

1. **Smart Contract Code**: A deployed `AgeVerification` contract handles proof validation.  
2. **Transaction Records**: Stores all function calls and input parameters for transparency.  
3. **State Data**: Maintains a mapping of verified users and their age verification status.  
4. **Event Logs**: Logs results of age verification for audit purposes.

---

## Integration with DigiLocker

SecureVault is designed to integrate seamlessly with applications like **DigiLocker**, which store official user documents. By accessing these documents securely, we can validate specific fields without exposing unnecessary information.

---

## Future Vision

Our long-term goal is to develop **SecureVault API Generator**, enabling third-party applications to request and verify any specific field based on their requirements. For instance:
- A financial application may verify creditworthiness.  
- A university might validate educational qualifications.  
- A rental service could confirm employment status.

---

## Tech Stack

- **IPFS**: Decentralized storage for user data.  
- **Zokrates**: ZKP generation and validation.  
- **Smart Contracts**: Blockchain-based proof validation and access management.
- **Solidity**: Smart contracts written in Solidity.
- **Frontend**: User-friendly interface for entering CID and verification details and document upload .
- **Backend**: API handling, data retrieval, and ZKP integration.

