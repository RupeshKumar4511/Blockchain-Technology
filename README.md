# Blockchain:
Blockchain is a distributed immutable ledger which is completely transparent.
The main purpose of Blockchain is deccentralization .
In January 2009 Santoshi Nakamoto created the first cryptocurrency Bitcoin.

# Metamask:
MetaMask is a software cryptocurrency wallet used to interact with the Ethereum blockchain.

<img width="273" alt="1" src="https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/5b5cd6b2-f495-4aa3-8c71-0ad236c7e170">

# Geth (Go ethereum):
Geth is a command line interface for running ethereum node implemented in Go language.
Using Geth we can join etherium network, transfer ether between accounts or mine ethers.


# How to make a private blockchain network:

1) Install Geth on Your System.
   
2) Create a Folder For Private Ethereum.
   
3) Make a genesis.json file for gensis block.
     
4) Execute genesis file
   
   geth --datadir ./data init ./genesis.json

5) Initialize the private network
    
    geth --datadir .\data\ --nodiscover 


# How to connect with Ethereium mainnet
On cmd type :   geth attach ipc://./pipe/geth.ipc

# How to create account on the Ethereum Mainnet:
On cmd type :    personal.newAccount()

And then create your password.


# How to mine on the Ethereum Private Network:
After creating account on cmd type;

miner.setEtherbase(eth.accounts[0])

miner.start(1)

And then miner balanced can be checked by Typing;

eth.getBalance(eth.accounts[0])

# 
sudo docker pull devopstestlab/solgraph
mkdir data
cd data
vim 


contract MyContract {  uint balance;

  function MyContract() {
    Mint(1000000);
  }

  function Mint(uint amount) internal {
    balance = amount;
  }

  function Withdraw() {
    msg.sender.send(balance);
  }

  function GetBalance() constant returns(uint) {
    return balance;
  }
}

docker run -it --rm -v $PWD:/data devopstestlab/solgraph
