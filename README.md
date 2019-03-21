Python Blockchain Example
-------------------------

This is a simple example how a blockchain works, including a JSON REST api.

##### Installation
* Make sure Python 3.6+ is installed

````
# start virtual environment and install dependencies

$ virtualenv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
````

Run the API with
````
$ python blockchain.py
$ python blockchain.py -p 5001
$ python blockchain.py -p 5002
````

Start mining with a GET request to
    
    http://localhost:5000/mine
    
Create a transaction with a POST request to

    http://localhost:5000/transactions/new
    
    example request body
    {
        "sender": "49eef747f8bc485387f1d4b93d63a512",
        "recipient": "a address",
        "amount": 5
    }
    
Get actual chain with a GET request

    http://localhost:5000/chain
    
    
#### Consensus
If you are running more then one node(miner) you have to be clear you use the right chain.
To resolve this, we first register our node to the network with a POST request:

    http:/localhost:5000/nodes/register
    
Then before start mining make sure you have the longest chain from the network with a GET

    http://localhost:5000/nodes/resolve
    
