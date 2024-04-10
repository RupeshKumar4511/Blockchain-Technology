# Blockchain:
Blockchain is a distributed immutable ledger which is completely transparent.
The main purpose of Blockchain is deccentralization.
In January 2009 Santoshi Nakamoto created the first cryptocurrency Bitcoin.

# Metamask:
MetaMask is a software cryptocurrency wallet used to interact with the Ethereum blockchain.

<img width="273" alt="1" src="https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/5b5cd6b2-f495-4aa3-8c71-0ad236c7e170">

# Geth (Go ethereum):
Geth is a command line interface for running ethereum node implemented in Go language.
Using Geth we can join etherium network, transfer ether between accounts or mine ethers.


# How to make a private blockchain network:

1) Install Geth on Your System.
   
2) Create a Folder (i.e Private Ethereum).
   
3) Make a genesis.json file for the gensis block and save into that folder.

   <img width="233" alt="image" src="https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/6112c12f-c4c3-4c99-9e96-a05a5cdc5c5f">

     
5) Execute the genesis file by run the commands on terminal, given below.
   
   geth --datadir ./data init ./genesis.json

6) And then Initialize the private network by run command :
    
    geth --datadir .\data\ --nodiscover 


# How to connect with Ethereium mainnet
On cmd run command :   geth attach ipc://./pipe/geth.ipc

# How to create account on the Ethereum Mainnet:
On cmd run command:    personal.newAccount()

And then create your password.


# How to mine on the Ethereum Private Network:
After creating account , run the folllowing the commands ;

miner.setEtherbase(eth.accounts[0])

miner.start(1)

And then miner balanced can be checked by run the following commmand;

eth.getBalance(eth.accounts[0])

# How to Visualize Solidity smart contracts:
step 1.) **install the docker on OS.**
step 2.) **pull the solgraph image by run this command on terminal :**  sudo docker pull devopstestlab/solgraph
step 3.) **make a directory :** mkdir data
step 4.) **change the directory :** cd data
step 5.) **Run the command :** vim -vi
**And then write the smart contract and save the contract file with .sol extension.**

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

step 6.) **Then run the command :** docker run -it --rm -v $PWD:/data devopstestlab/solgraph

![Screenshot from 2024-04-08 19-20-26](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/e9924da9-6068-45bd-95a4-8e65d792b64c)



![Screenshot from 2024-04-08 19-31-26](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/748f3397-e2ec-465b-bed1-90f41b80498a)

#audits
![Screenshot from 2024-04-10 20-37-12](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/2fdc2805-d8e8-41ff-a38e-dfd1022592bb)

![Screenshot from 2024-04-10 21-07-49](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/28da7532-5797-42d9-b1d0-6fa7d3fbf6b0)

![Screenshot from 2024-04-10 21-17-14](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/b67acc92-92c8-4e0a-90e3-2f017fe2ff88)

