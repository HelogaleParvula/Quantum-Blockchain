# Quantum Blockchain in Python

In this Global Qiskit Hachathon by IBM, we propose a project where we flip the classical paradigm of a blockchain and create a blockchain using quantum mechanics. The project is written in python, and uses the celebrated Python library for quantum computation and quantum information 'Qiskit'. The main code in this project is located in the file named *Blockchain.ipynb*. In this interactive notebook the two main objects in the project are defined: nodes and blockchain. Both contain the essential methods required by a full working blockchain to work: create hash states, create blocks, add transactions...

## Class node
Starts by initializing the number of nodes, an index to identify them and the first transactions paths and transaction count.
It contains the *transaction function* which verifies that the transaction can be made by checking that the funds in the wallet are greater than the transaction to be made. If true, rewrites the wallet of the involving nodes.
The *create_block* function creates a text file containing the transaction of the previous block, the previous state, transactions and the block number. It stores the information of the winning node and sets the payments for solving the blocks and the maintenance reward. In addition, it stores the information of the previous fidelities.
*Update_winners* function sets who solves the block by obtaining the major fidelity. On the other hand, *write_fidelitiy* saves the fidelity table in a cvs file.
*State_ parameters* function hashes the block information, thanks to the *Sha256*  function, in two parts obtaining two parameters. To represent these parameters as a state in the block sphere it brings its values to (0,\pi) and (0,2\pi) obtaining this way θ, ϕ, which determines only one state.

## Class blockchain
This class creates a new blockchain. First, parameters which describe the blockchain are initialized: number of nodes, allowed transactions per block, , and the length of the random numbers involved. After parameters, attributes are deffined. Appart from the previously mentioned, a list of the nodes indices and a list of the nodes in the chain are provided.
Then, three .csv files are created for each node in order to record transactions, fidelities and blocks.

The corresponding functions are described as follows: 
*initialize_files* a initial transactions file is inizialited giving each node 20 coins to make transactions.
*random_numbers* creates as many sequences of random numbers as nodes by means of *random_digits*. Those numbers are generated using a quantum generator and are used to verify the block at the end of the process. 
*send_states* is used to simulate the process of sending a state between two nodes using quantum teleportation.
*fidelity_table* simulates the process of measuring all possible fidelities between nodes.
*get_winners* search the maximum fidelities between all the calculated ones.
*update_blocks* tells the nodes about the winner node in order to get the blocks updapted. Also, gives the reward to the winners.
*solve_block* verifies the blocks of the winners by means of the calculation of fidelities and the random numbers
*add_transactions* enables user to add to the blockchain a particular transaction specifying nodes and the amount.
