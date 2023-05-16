# Sequence Data Repository using block_chain concept
@Author: Sanjana Sharma

This is Python implementation for storage and management of the fasta sequences using BlockChain. 
It has the following features:
Creation of a genesis block with a given FASTA sequence
Addition of new blocks with a given FASTA sequence, associated ID, and version changes
Versioning of FASTA sequences
Checking and printing the blockchain


## Requirements
Python 3.x

## Usage 

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

