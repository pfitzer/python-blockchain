Python Blockchain Example
-------------------------

This is a simple example how a blockchain works, including a JSON REST api.

Run the API with
````
$ python blockchain.py
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
    
