# Personal Python Blockchain implementation
My own personal simple, local, blockchain implementation using Python.


## Installation

1. Make sure [Python 3.6+](https://www.python.org/downloads/) is installed.
2. Install [pipenv](https://github.com/kennethreitz/pipenv) to create our local environment and either [cURl](https://curl.haxx.se/download.html) or [Postman](https://www.getpostman.com/apps) to interact with our API over our local network.

```
$ pip install pipenv
```

3. Create a _virtual environment_ and specify the Python version to use.

```
$ pipenv --python=python3.6
```

4. Install requirements.  

```
$ pipenv install
```

5. Run the server:
```
$ pipenv run python blockchain.py
```

## Usage

1. Start the server:

```
$ python blockchain.py
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

2. In order to register new nodes simply create a new process to localhost on a new port or with another machine.

### Mining

Make a GET request to http://localhost:5000/mine

### Create a Transaction

Make a POST request to http://localhost:5000/transactions/new with a body fulfilling this transaction structure:
```
{
 "sender": "your-address",
 "recipient": "someone-other-address",
 "amount": 1
}
```
