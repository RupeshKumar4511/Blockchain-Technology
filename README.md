# Blockchain:
Blockchain is a distributed immutable ledger which is completely transparent.
The main purpose of Blockchain is deccentralization.
In January 2009 Satoshi Nakamoto created the first cryptocurrency Bitcoin.

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
**On cmd run command :** 

       geth attach ipc://./pipe/geth.ipc 

# How to create account on the Ethereum Mainnet:
**On cmd run command:**   

        personal.newAccount()

**And then create your password.**


# How to mine on the Ethereum Private Network:
**After creating account , run the following the commands ;**

          miner.setEtherbase(eth.accounts[0])

          miner.start(1)

**And then miner balanced can be checked by run the following commmand;**

          eth.getBalance(eth.accounts[0])

# How to Visualize Solidity smart contracts:

1.) **install the docker on OS.**

2.) **pull the docker image for solgraph by run this command on terminal :**

          sudo docker pull devopstestlab/solgraph

**Solgraph:** A tool to generate a DOT graph that visualises the function control flow of a Solidity contract and highlights potential security vulnerabilities.

3.) **make a directory :** 

           mkdir data
           
4.) **change the directory :** 

           cd data
           
5.) **Run the command :** 

           vim -vi
           
**And then write the smart contract and save the contract file with .sol extension.(i.e for example Mycontract.sol)**

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/b926bbab-df4b-432a-a63a-c8461406d2f5)



6.) **Then run the command :** 

          docker run -it --rm -v $PWD:/data devopstestlab/solgraph 

![Screenshot from 2024-04-08 19-20-26](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/e9924da9-6068-45bd-95a4-8e65d792b64c)



![Screenshot from 2024-04-08 19-31-26](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/748f3397-e2ec-465b-bed1-90f41b80498a)

# Security audits for smart contract using slither:

**Slither:** An Solidity static analysis framework. Through its printers, it can map method visibility and modifiers, state variables that are read and written, identify calls, and print the inheritance graph of a smart contract.

1.) **pull the docker image for slither by run this command on terminal :**

            docker pull trailofbits/eth-security-toolbox
      
2.) **make a directory :** 

           mkdir audit
           
3.) **change the directory :** 

           cd audit
           
4.) **Run the command :** 

           vim -vi
           
**And then write the smart contract and save the contract file with .sol extension.(for example SimpleStorage.sol)**

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/fa046006-a95b-4cc9-ad4c-ffdf3bb0f7ec)



5.) **Then run the command :** 

       docker run -it --rm -v $PWD:/data trailofbits/eth-security-toolbox

![Screenshot from 2024-04-10 20-37-12](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/2fdc2805-d8e8-41ff-a38e-dfd1022592bb)

6.)**Open another terminal and Run the command to obtain container id:**

        sudo docker container ls
   
7.)**And then Run the command:**

        sudo docker cp $(pwd)/filename.sol “containner-id”:/home/ethsec

8.)**Run the command in the first terminal:**

       slither filename.sol
    
![Screenshot from 2024-04-10 21-07-49](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/28da7532-5797-42d9-b1d0-6fa7d3fbf6b0)

9.)**And then Run another command in the first terminal:**

      slither-check-erc filename.sol <contract name in code>
    
![Screenshot from 2024-04-10 21-17-14](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/b67acc92-92c8-4e0a-90e3-2f017fe2ff88)

# Security audits for smart contract using Mythril:

1) **pull the docker image for Mythril by run command**

      sudo docker pull mythril/myth
   
2) **make a directory**
   
      mkdir audits2
   
3) **change the directory**
   
      cd audits2
   
4) **run the command**
   
      vim -vi
   
5) **And then write the smart contract and save the contract file with .sol extension.(for example Ballot.sol)**

![Screenshot from 2024-04-12 20-22-15](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/e3f9e36d-f662-498d-b0b8-09d0feb62ede)
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/9d0301c7-9598-48c5-8557-4bb6f8dca538)
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/180a6025-e6af-465f-bfcd-180b71bdb64a)

6) **To analyse the smart contract run the command**

        myth analyze Ballot.sol

![Screenshot from 2024-04-12 18-30-18](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/c9a377d8-e785-41b9-9161-61da2e4c2248)

# Security audits for smart contract using Surya:

1) **install npm by run the command**
   
      sudo apt install npm
   
2) **install surya**
   
     sudo npm install -g surya

3) **make a directory**
   
     mkdir audits2

4) **change the directory**
   
     cd audits2

5) **run command**
    
     vim -vi


6) **And then write the smart contract and save the contract file with .sol extension.(for example 
   Storage.sol)**
   
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/fa046006-a95b-4cc9-ad4c-ffdf3bb0f7ec)

7) **Then run the command**
   
      surya parse Storage.sol

**Parse :**  The parse command outputs a treefied AST object coming from the parser.
    
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/64512083-d3f3-4f0d-9ff6-2901cefffdee)
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/7cd48a08-f422-42dc-ac0c-9ceab737931d)
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/cad3956c-ce25-4859-a906-6a5985580cb3)

8) **Then run another command**
   
       surya flatten Storage.sol
   
**Flatten :** The flatten command outputs a flattened version of the source code, with all import statements replaced by the corresponding source code. Import statements that reference a file that has already been imported, will simply be commented out.

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/950a5975-992b-40ff-936b-3d268b1c90a8)

# Security audits for solidity smart contract using manticore:

1) **pull the docker image for manticore**

         sudo docker pull trailofbits/manticore
    
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/0175889b-ab4b-421b-9694-90cdf20570c8)

2) **make a directory**
   
      mkdir audits2
   
3) **change the directory**
   
      cd audits2
   
4) **run the command**
   
      vim -vi
   
5) **And then write the smart contract and save the contract file with .sol extension.(for example Storage.sol)**
   
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/fa046006-a95b-4cc9-ad4c-ffdf3bb0f7ec)


6) **Then run command**
   
      manticore Storage.sol

# How to make dapp(decentralized application):
1)Set the environment
   ```bash
   sudo apt update
   sudo apt install curl git
   curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
   sudo apt-get install -y nodejs
```


![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/0f0e5f5b-475b-4e6a-81fe-e857d15894bf)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/73e26677-5701-4f89-b0f4-8e5e7366377f)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/87dedc4c-763d-4652-8544-3b191b8b9409)


```solidity
pragma solidity ^0.8.0;


// This is the main building block for smart contracts.
contract Token {
    // Some string type variables to identify the token.
    string public name = "My Hardhat Token";
    string public symbol = "MHT";

    // The fixed amount of tokens, stored in an unsigned integer type variable.
    uint256 public totalSupply = 1000000;

    // An address type variable is used to store ethereum accounts.
    address public owner;

    // A mapping is a key/value map. Here we store each account's balance.
    mapping(address => uint256) balances;

    // The Transfer event helps off-chain applications understand
    // what happens within your contract.
    event Transfer(address indexed _from, address indexed _to, uint256 _value);

    /**
     * Contract initialization.
     */
    constructor() {
        // The totalSupply is assigned to the transaction sender, which is the
        // account that is deploying the contract.
        balances[msg.sender] = totalSupply;
        owner = msg.sender;
    }

    /**
     * A function to transfer tokens.
     *
     * The `external` modifier makes a function *only* callable from *outside*
     * the contract.
     */
    function transfer(address to, uint256 amount) external {
        // Check if the transaction sender has enough tokens.
        // If `require`'s first argument evaluates to `false` then the
        // transaction will revert.
        require(balances[msg.sender] >= amount, "Not enough tokens");

        // Transfer the amount.
        balances[msg.sender] -= amount;
        balances[to] += amount;

        // Notify off-chain applications of the transfer.
        emit Transfer(msg.sender, to, amount);
    }

    /**
     * Read only function to retrieve the token balance of a given account.
     *
     * The `view` modifier indicates that it doesn't modify the contract's
     * state, which allows us to call it without executing a transaction.
     */
    function balanceOf(address account) external view returns (uint256) {
        return balances[account];
    }
}
```
   
![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/fb31ea8f-a7a4-41c5-ab97-d3baa9dd7dac)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/9f4336f2-7711-497e-a6a7-e376433e0679)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/f5d6ed1d-dc6b-49ce-a587-377cc4f14c18)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/9ebbc8d0-3245-4da3-89d6-42f0edd7e41d)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/2f03de7e-bc77-4410-a4df-5c4cdb8b1d2d)

![image](https://github.com/RupeshKumar4511/Blockchain-Technology/assets/149661006/33832d08-cb15-464e-b2a4-80327c9f2e80)

