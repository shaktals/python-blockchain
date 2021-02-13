# A rudimentary blockchain implementation in python.

## To run it:

1) Execute the 3 nodes (DeJair, Djou, ManoVei) locally in 3 separate terminals that can run python3 (e.g.: _python3 DeJair_node.py_)
2) You are then ready to interact with the nodes using a REST client

## To interact with it:

- First connect each node by making a POST request to http://localhost:{node_address}/connect_node with a JSON payload like the example at _nodes.json_
(remember to exclude from the JSON list the node address against which the request is made, as the node doesn't need to connect with itself)

You can then play with the other 5 routes available:

- POST http://localhost:{node_address}/add_transaction
To add a transaction, including a JSON payload following the model at _transaction.json_
- GET http://localhost:{node_address}/get_chain
To see the current status of the blockchain on a node
- GET http://localhost:{node_address}/is_valid
To confirm the blockchain on a node has a valid state
- GET http://localhost:{node_address}/mine_block
To mine a block, including all transactions that were added on that node
- GET http://localhost:{node_address}/replace_chain
To sync a node chain with all the other nodes, the longest valid chain wins
