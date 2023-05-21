# Sequence Data Repository using block_chain concept
@Author: Sanjana Sharma

This is Python implementation for storage and management of the fasta sequences using BlockChain. 
It has the following features:
Creation of a genesis block with a given FASTA sequence
Addition of new blocks with a given FASTA sequence, associated ID, and version changes
Versioning of FASTA sequences
Checking and printing the blockchain


## Requirements
Interface :
Python 3.x
Required Libraries :
json, hashlib, time

## Usage 
1. Import the necessary libraries.
```python
import json
import hashlib
import time
```
2. Define the Block Class
```python
class Block:
    def __init__(self, index, timestamp, data, previous_hash, version_changes):
        # ...
 ```
3. Define the Blockchain Class
```python
class BlockChain:
    def __init__(self, genesis_fasta):
        # ...
```
4. Usage 
```
Create a blockchain instance:
```python
blockchain = BlockChain(genesis_fasta)
```
```
Check the blockchain for versioning and simultaneously add the block:
```python
blockchain.check_version(id, fasta)
```
```
Print the blockchain:
```python
blockchain.print_blockchain()
```

Example
```python

# Create a blockchain with a given FASTA sequence
blockchain = BlockChain("GATTACA")

# Check the blockchain for versioning and the block directly if it doesn't exist or if it exists its version shall be updated
blockchain.check_version("Sequence 1", "GATTCAC")

# Print the blockchain
blockchain.print_blockchain()
```
5. The above one explained the usuage of the blockchain from scratch, instead the below package could be utilized for performing the same task.
```python
#installing package
pip install genochain

#importing package
from genochain.genochain import BlockChain

#genesis block creation
blockchain = BlockChain("AUG")

#importing fasta sequences into blockchain                     
blockchain.check_version('seq1','GAATTTCC')
blockchain.check_version('seq1','GTTTCC')

#Print the blockchain
blockchain.print_blockchain()
```

## Notes 
The code provided is a basic implementation of a blockchain and may not include all the necessary features or security measures required for a production-level blockchain system.

The BlockChain class assumes that the genesis_fasta parameter passed to the constructor is a valid FASTA sequence.
The code can be extended or modified based on specific use cases or requirements.

Please refer to the provided code for a detailed implementation and explore the functions and classes for a better understanding of the blockchain implementation.

Important: Ensure you have fulfilled the requirements mentioned above before running the code.

Feel free to modify the code or adapt it to suit your needs.

## Disclaimer
The provided code is for educational and research purposes only and should not be used for critical or production systems without proper review, testing, and security considerations.

