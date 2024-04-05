# How to make a private blockchain network:
1)  make a genesis.json file for gensis block.
2)  geth --datadir "./data" account new
    Password:
    Repeat password: 
3)   geth --datadir ./data init ../genesis.json
4)   geth --datadir .\data\ --nodiscover 
