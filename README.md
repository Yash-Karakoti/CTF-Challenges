# Capture the Flag Challenges - Algorand

This repository contains solutions to three Capture the Flag (CTF) challenges on the Algorand Testnet. Each challenge involves using Algorand's smart contracts, transactions, encryption techniques, and Testnet functionality.

## Challenge 1: Where is the Flag?

In this challenge, the task was to uncover a hidden clue within a smart contract deployed on the Algorand Testnet. The clue, stored in global storage, could be found by analyzing one of the contract's transactions. Upon finding the clue, I decrypted it to reveal a wallet address, to which I then programmatically sent 1 Algo token.

### Details

**Receiver's Address (decrypted)**: 2JAZQO6Z5BCXFMPVW2CACK2733VGKWLZKS6DGG565J7H5NH77JNHLIIXLY
**Transaction sent**:[Transaction link](https://testnet.explorer.perawallet.app/tx/AMEMU2VI6S7H7F45JZR6WQTYXGSQDOABMCDWF7OA4FBXVKFK7Z2A)

**Transaction Confirmed in Round**: 44391591

### Terminal Output

```yaml
Address: IE5QFQSJ66RIERSW4O6BZHDJMFELM24AO2ULPNEB4ZWT6C3MUDDWNIBRCM
Txn sent: https://testnet.explorer.perawallet.app/tx/AMEMU2VI6S7H7F45JZR6WQTYXGSQDOABMCDWF7OA4FBXVKFK7Z2A
Txn Confirmed in Round: 44391591
```
### Image 

![Challenge 1](public/assets/ctf%201.png)

### Resources

[Smart Contract Apps and Global State in Algorand](https://developer.algorand.org/docs/get-details/dapps/smart-contracts/apps/state/)

## Challenge 2: Find the Hidden Flag

In this challenge, I was tasked with deciphering a hidden clue within six strings using substitution cipher techniques. The decrypted clue revealed an asset ID, and I then performed an opt-in transaction for the corresponding NFT.

### Strings to Decipher:
```bash
NJMLQSORQ
QOLSRJNQM
QLJNROSMQ
JLQRNMOSQ
JNQSQORLM
NQSJMROQL
```

## Solution

After using substitution cipher methods, I uncovered the following asset ID: 720485937

### Transaction

**Asset ID (task)**: 720485937

**Transaction sent**: [Transaction link](https://testnet.explorer.perawallet.app/tx/34C5GAOOX4MYFC4XO626IWCTTALKMFGVI7QGUMECYB7PUZVW5OYQ/)

**Transaction Confirmed in Round**: 44391578

### Terminal Output

```yaml
Address: IE5QFQSJ66RIERSW4O6BZHDJMFELM24AO2ULPNEB4ZWT6C3MUDDWNIBRCM
Txn sent: https://testnet.explorer.perawallet.app/tx/34C5GAOOX4MYFC4XO626IWCTTALKMFGVI7QGUMECYB7PUZVW5OYQ
Txn Confirmed in Round: 44391578
```

### Image

![Challenge 2](public/assets/Screenshot%202024-10-01%20202434.png)


## Challenge 3: Encryption and Algo Transfer

The third challenge involved using an Asset ID from Challenge 2 and a wallet address from Challenge 1 to form a key. This key was then used to encrypt the provided message using the HMAC-SHA256 algorithm. Finally, I sent 1 Algo to the specified wallet address with the encrypted message as a note.

### Key Formation:

**Wallet Address (Challenge 1)**: 2JAZQO6Z5BCXFMPVW2CACK2733VGKWLZKS6DGG565J7H5NH77JNHLIIXLY

**Asset ID (Challenge 2)**: 720485937

**Formed Key**: ZA2

### Encrypted Message:

**Original Message**: Algorand uses Pure Proof of Stake Algorithm.

**Encrypted Message (using HMAC-SHA256)**: ae6ebfcff2e1d10cafb51c0e4ab77da22838436dd3b5d82b7d2eb6104bd30dc3

### Transaction

**Transaction sent:**[Transaction Link](https://testnet.explorer.perawallet.app/tx/T7U7PRZOYN7OWVH2HKRYGBQ75MKYGDOTDDFQWWUVX33QHU6SF4CA/)

**Transaction Confirmed in Round**: 44391623

### Terminal Output:

```yaml
Message in encryption: ae6ebfcff2e1d10cafb51c0e4ab77da22838436dd3b5d82b7d2eb6104bd30dc3
Address: IE5QFQSJ66RIERSW4O6BZHDJMFELM24AO2ULPNEB4ZWT6C3MUDDWNIBRCM
Txn sent: https://testnet.explorer.perawallet.app/tx/T7U7PRZOYN7OWVH2HKRYGBQ75MKYGDOTDDFQWWUVX33QHU6SF4CA
Txn Confirmed in Round: 44391623
```

### Image

![Challenge 3](public/assets/Screenshot%202024-10-01%20202737.png)

## Conclusion

These challenges required knowledge of smart contracts, cryptography, and transaction handling in Algorand. All transactions were successfully executed on the Algorand Testnet, fulfilling the required tasks for each challenge.


