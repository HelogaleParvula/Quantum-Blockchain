The principal part of the code is the file named *Node_Blockchain_class*. As its name indicates, it is made up of two central classes, class node and class blockchain.

**Class node:** 






**Class blockchain:** this class creates a new blockchain. First, parameters which describe the blockchain are initialized: number of nodes, allowed transactions per block, , and the length of the random numbers involved. After parameters, attributes are deffined. Appart from the previously mentioned, a list of the nodes indices and a list of the nodes in the chain are provided.
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
