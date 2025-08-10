---
title: "Unveiling the Mysteries: Public Key, Private Key, and Address in the Ethereum Realm"
datePublished: Sun Jul 21 2024 15:47:39 GMT+0000 (Coordinated Universal Time)
cuid: clyvqeuiv000q09jl7g5b7vht
slug: mysteries-public-key-private-key
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1721576752839/b5be0832-229a-467f-a43f-d30730abb9aa.jpeg
tags: encryption, blockchain, cryptography, cryptocurrency, ethereum, hashing

---

The world of Ethereum and blockchain technology is both fascinating and complex, filled with unique cryptographic components that work in harmony to secure and manage digital assets. Among these components, three fundamental elements stand out: the private key, the public key, and the Ethereum address. Understanding the differences between these keys and their roles is crucial for anyone navigating the Ethereum landscape. Let’s dive into the intriguing details of each.

# The Secret Keeper: Private Key

* **Length**: 32 bytes
    
* **Role**: The private key is the cornerstone of your Ethereum account. This 256-bit number is randomly generated and must remain a closely guarded secret. It’s akin to a master password that grants full control over your Ethereum account. When you sign a transaction, it's the private key that authorizes it.
    
* **Security**: Losing your private key means losing access to your assets. If someone else obtains it, they can take complete control of your account.
    

# The Verifier: Public Key

* **Length**: 64 bytes (uncompressed) or 33 bytes (compressed)
    
* **Role**: The public key is derived from the private key through a cryptographic process called elliptic curve multiplication. It’s used to verify the authenticity of signed transactions, ensuring they were indeed signed by the owner of the corresponding private key.
    
* **Visibility**: Although not typically displayed in day-to-day Ethereum transactions, the public key plays a vital role behind the scenes.
    

# The Identifier: Ethereum Address

* **Length**: 20 bytes
    
* **Role**: The Ethereum address is the user-friendly identifier derived from the public key. Specifically, it’s the last 20 bytes of the Keccak-256 hash of the public key. Think of it as a shortened, more manageable representation that you can share with others to receive Ether or tokens.
    
* **Format**: An Ethereum address usually starts with "0x" followed by 40 hexadecimal characters, e.g., `0x742d35Cc6634C0532925a3b844Bc454e4438f44e`.
    

## Didn't get the above!, read again in other words

### Private Key

* **Description**: A private key is a randomly generated 256-bit number that serves as the key to a user's account and is kept secret. It is the most crucial piece of information for an Ethereum user because it provides full access to the associated account.
    
* **Use Case**: The private key is used to sign transactions, allowing the holder to authorize operations like sending Ether or interacting with smart contracts.
    
* **Security**: Must be kept secure and private. If someone gains access to your private key, they can fully control your Ethereum account.
    

### Public Key

* **Description**: The public key is derived from the private key using elliptic curve cryptography (specifically, the secp256k1 curve). It is a 512-bit number (128 hexadecimal characters).
    
* **Use Case**: The public key is used to verify the signature of a transaction. When a transaction is signed with a private key, the corresponding public key can be used to confirm that the transaction was indeed signed by the owner of the private key.
    
* **Visibility**: While the public key itself is not directly visible in common Ethereum transactions, it can be computed from the address.
    

### Address

* **Description**: An Ethereum address is derived from the public key by taking the last 20 bytes (40 hexadecimal characters) of the Keccak-256 hash of the public key. This process ensures that the address is a shorter and more manageable identifier.
    
* **Use Case**: The address is used to identify accounts on the Ethereum blockchain. It is what you share with others to receive Ether or tokens and to interact with smart contracts.
    
* **Format**: Ethereum addresses typically start with "0x" followed by 40 hexadecimal characters, e.g., `0x742d35Cc6634C0532925a3b844Bc454e4438f44e`.
    

### Relationship Between Them

1. **Private Key -&gt; Public Key**:
    
    * The private key generates the public key using elliptic curve multiplication.
        
    * This operation is one-way and secure; you cannot derive the private key from the public key.
        
2. **Public Key -&gt; Address**:
    
    * The public key is hashed using the Keccak-256 algorithm, and the last 20 bytes of this hash become the Ethereum address.
        
    * This ensures that the address is a compact, unique identifier for the public key.
        

### Connecting the Dots

1. **Generating the Private Key**:
    
    * A private key is a 32-byte number, fundamental to securing your Ethereum account.
        
    * Example: `0x4c0883a69102937d6231471b5dbb6204fe512961708279c7aef88a7f5588c27e`.
        
2. **Deriving the Public Key**:
    
    * From the private key, the public key is derived, which can be either 64 bytes (uncompressed) or 33 bytes (compressed).
        
    * Example: `0x5a2b1f5b2ec4b6e0cbfa527f68cd295b7e6e1a8b703fb8de9b507b5958ad270bbf5aa9a0c2e8822b1421c2ab31d1cabaea6ad6b31c8f8a2d7e8a7ff4ac3fdf75`.
        
3. **Creating the Ethereum Address**:
    
    * The Ethereum address is derived by taking the last 20 bytes of the Keccak-256 hash of the public key.
        
    * Example: `0x742d35Cc6634C0532925a3b844Bc454e4438f44e`.
        

### Example Flow

1. **Generate a Private Key**:
    
    * A private key is randomly generated.
        
    * Example: `0x4c0883a69102937d6231471b5dbb6204fe512961708279c7aef88a7f5588c27e`
        
2. **Derive the Public Key**:
    
    * The public key is derived from the private key.
        
    * Example: `0x5a2b1f5b2ec4b6e0cbfa527f68cd295b7e6e1a8b703fb8de9b507b5958ad270bbf5aa9a0c2e8822b1421c2ab31d1cabaea6ad6b31c8f8a2d7e8a7ff4ac3fdf75`
        
3. **Compute the Address**:
    
    * The address is derived from the public key by taking the last 20 bytes of the Keccak-256 hash.
        
    * Example: `0x742d35Cc6634C0532925a3b844Bc454e4438f44e`
        

### Here are the lengths of each entity in bytes within the Ethereum domain:

1. **Private Key**
    
    * **Length**: 32 bytes
        
    * **Description**: A private key is a 256-bit number, which is 32 bytes in length.
        
2. **Public Key**
    
    * **Length**: 64 bytes (uncompressed) or 33 bytes (compressed)
        
    * **Description**:
        
        * The uncompressed public key is 512 bits (64 bytes), derived directly from the private key using elliptic curve multiplication.
            
        * The compressed public key is 33 bytes, including an extra byte to indicate whether the y-coordinate is even or odd.
            
3. **Address**
    
    * **Length**: 20 bytes
        
    * **Description**: An Ethereum address is derived from the last 20 bytes of the Keccak-256 hash of the public key. This results in a 160-bit (20 bytes) address.
        

### Summary

* **Private Key**: 32 bytes
    
* **Public Key**: 64 bytes (uncompressed) or 33 bytes (compressed)
    
* **Address**: 20 bytes
    

## Doubts/Questions

### `Can I get the public key from the address?`

In the Ethereum domain, you cannot directly derive the public key from an Ethereum address. The process of generating an Ethereum address from a public key is a one-way function. Here’s a more detailed explanation of why this is the case and what the implications are:

### One-Way Cryptographic Process

1. **Private Key to Public Key**:
    
    * The public key is derived from the private key using elliptic curve multiplication (secp256k1 curve). This process is computationally easy in the forward direction (private key to public key) but infeasible to reverse.
        
2. **Public Key to Address**:
    
    * The Ethereum address is generated by taking the last 20 bytes of the Keccak-256 hash of the public key. This hashing process is designed to be a one-way function, meaning you cannot easily retrieve the original public key from the address.
        

### Implications

* **Security**: This one-way property ensures that even if someone knows your Ethereum address, they cannot deduce your public key or private key from it. This enhances the security of your account.
    
* **Transaction Verification**: When you send a transaction, the signature (created using your private key) can be verified against the public key. While the public key is not directly visible, it can be inferred by the network during transaction verification.
    
* **Recovering Public Key from Transaction**: The only scenario where a public key can be derived is from a signed transaction. When a transaction is signed, the signature includes enough information for the network to recover the public key used to sign the transaction. However, this is an indirect method and involves analyzing the transaction itself.
    

### `So, can I ask the Ethereum network for the public key associated with an address?`

No, you cannot request or retrieve the public key associated with an Ethereum address directly from the Ethereum network. Here’s why:

### Why You Can't Retrieve the Public Key

1. **Address vs. Public Key**:
    
    * **Address**: An Ethereum address is derived from the public key through a one-way hashing process. This hashing ensures that while you can derive an address from a public key, you cannot reverse this process to get the public key from the address.
        
2. **Privacy and Security**:
    
    * **Security**: Ethereum addresses are designed to be a shorter, more manageable form of public keys. The network does not store or expose public keys directly for addresses to ensure privacy and security.
        
3. **Public Key Recovery**:
    
    * **Signed Transactions**: The only way to derive the public key associated with an address is through a signed transaction. If you have a transaction signed by the address, you can recover the public key from the signature. This is typically done using libraries like `ethers.js` or `web3.js`.
        

### `So, does each network have a different public key associated with a different address, and can the public key be different on different networks with the same addresses?`

In the Ethereum ecosystem, public keys, private keys, and addresses are consistent across different networks (e.g., Ethereum mainnet, Ropsten, Rinkeby) as long as the same private key is used. Here’s how it works:

### Consistency Across Networks

1. **Private Key**:
    
    * A private key is a 256-bit number that remains the same regardless of the network. If you generate a private key, it will be identical whether you use it on the Ethereum mainnet, a testnet (like Ropsten, Rinkeby), or any Ethereum-compatible network.
        
2. **Public Key**:
    
    * The public key is derived from the private key using the elliptic curve cryptography (secp256k1). Since the private key is the same, the public key will also be the same across different networks.
        
3. **Address**:
    
    * An Ethereum address is derived from the public key by taking the last 20 bytes of the Keccak-256 hash of the public key. Since the public key is the same, the Ethereum address will also be the same across different networks.
        

### `So, will this be different on different blockchains like Solana?`

Yes, the keys and addresses are different on different blockchain platforms like Solana. Here's a detailed explanation:

### Different Blockchains, Different Cryptographic Systems

1. **Ethereum**:
    
    * **Private Key**: A 256-bit number.
        
    * **Public Key**: Derived from the private key using the secp256k1 elliptic curve.
        
    * **Address**: The last 20 bytes of the Keccak-256 hash of the public key.
        
2. **Solana**:
    
    * **Private Key**: Uses Ed25519, which is a different elliptic curve system.
        
    * **Public Key**: Derived from the private key using the Ed25519 elliptic curve.
        
    * **Address**: Solana uses the public key directly as the address (typically represented in Base58).
        

### Key Differences

1. **Cryptographic Algorithms**:
    
    * Ethereum uses secp256k1 for its elliptic curve cryptography.
        
    * Solana uses Ed25519 for its elliptic curve cryptography.
        
2. **Address Format**:
    
    * Ethereum addresses are 20 bytes derived from the Keccak-256 hash of the public key.
        
    * Solana addresses are directly derived from the public key and are typically represented in Base58 format.