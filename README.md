# Python--Blockchain
This project involves creating a basic blockchain and understanding the working of BlockChain Technology. The code creates a simple blockchain with two blocks – Genesis and the next.

3 components involved in running the Block Chain Technology are
Block – which contains the transaction details
Clients – Who make the transactions
Miner – Who collects the transactions, validates them and mines a block
Blockchain is a data structure that chains all the mined blocks in chronological order. This chain is immutable and thus tamper-proof.

'Block' Class:
The 'Block' class represents an individual block in the blockchain. Each block has the following attributes:
'timestamp': A timestamp indicating when the block was created.
'data': The data or transactions stored in the block.
'previous_hash': The hash of the previous block in the blockchain.
'hash': The hash of the current block, calculated using the 'calculate_hash' method. The 'calculate_hash' method computes the SHA-256 hash of the concatenated string of timestamp, data, and previous hash.

'Client' Class:
The 'Client' class represents a client interacting with the blockchain. It has the following methods:
     -'add_new_transaction': Adds a new transaction to the blockchain through the 'add_new_transaction' method of the blockchain.
     -'mine': Mines a new block using the 'mine' method of the blockchain.

'Blockchain' Class:
The 'Blockchain' class manages the entire blockchain. It has the following attributes and methods:
                       -'chain': A list to store blocks.
                       -'unconfirmed_transactions': A list to store transactions that are not yet added to a block.
The 'create_genesis_block' method creates the initial or "genesis" block with some default data ("Genesis Block").
The 'get_latest_block' method returns the last block in the blockchain.
The 'add_new_transaction' method adds a new transaction to the list of unconfirmed transactions.
The 'mine' method creates a new block with the unconfirmed transactions, links it to the latest block, and adds it to the blockchain.
The 'add_block' method is used to add a new block to the blockchain. It updates the previous hash and calculates the new block's hash.

A 'Blockchain' object is created.
A 'Client' object is created with the blockchain instance.
A new transaction is added to the blockchain, and a block is mined.
Another transaction is added, and another block is mined.
The blockchain is printed to the console, showing the details of each block.
