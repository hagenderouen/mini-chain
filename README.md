# Mini-chain
Run a virtual blockchain on your local computer. Special thanks to [Hadelin de Ponteves](https://www.udemy.com/user/hadelin-de-ponteves/)

## Tools
* Any Python IDE
* [Flask](https://flask.palletsprojects.com/en/1.1.x/)
* [Postman](https://www.getpostman.com/)
* [Remix Etherium](https://remix.ethereum.org)

## Blockchain Demo
Get the blockchain, mine blocks, and check if the blockchain is valid.

1. Run blockchain.py using Python IDE
2. Using Postman, send requests to http://127.0.0.1:5000/
### GET methods
* get_chain - gets the full blockchain
* mine_block - mines a new block
* is_valid - checks if the blockchain is valid

## Cryptocurrency 'Hadcoin' Demo
Connect the blockchain nodes, add transactions, and mine blocks. For any blocks added, get consensus by calling replace_chain. Get the blockchain and check if it is valid.

1. Run hadcoin_node_[port].py in separate consoles.
2. Using Postman, send requests to http://127.0.0.1:[port]/
3. Send POST /connect_node requests to all nodes. Paste nodes.json in request body. Remove receiving node from the post request body. For example, if sending POST /connect_node to http://127.0.0.1:5001/ remove http://127.0.0.1:5001/ from the POST request body.
5. Send GET /mine-block to any node.
6. Send POST /replace_chain on other nodes.
7. Send POST /add_transaction to any node using. Pase transaction.json in request body. Replace sender and receiver strings with any name, and amount with integer.
8. Send GET /mine_block to mine the transaction to the blockchain.
9. Send POST /replace_chain on other nodes.

### GET methods
* get_chain
* mine_block
* is_valid

### POST methods
* connect_node - connects new nodes
* add_transaction - adds a new transaction to the blockchain
* replace_chain - replaces the chain with the longest chain if needed

## Etherium Smart Contract
Compile, deploy, and run transactions using Remix Etherium.
Paste hadcoins_ico.sol into main panel.
