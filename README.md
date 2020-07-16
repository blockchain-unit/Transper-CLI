#Transper-CLI

The repo contains CLI to the run prototype of Transper

## Requirements
Docker 19
## Instructions to set up Docker Image of Transper



Download the image from [here](https://drive.google.com/file/d/1CceQNBz9utHHROThlKv013ND3S5785TH/view?usp=sharing)
Run the following command to load the image
```bash
docker load -i <path to image tar file>

```

## Running Tool

```bash
docker run -v <path to contract>:/home/contracts/Contract.sol --rm pythonimage /home/contracts/Contract.sol <contract name> <contract address>
```
e.g
```bash
docker run -v /home/examples/Indoaset.sol:/home/contracts/Contract.sol --rm pythonimage /home/contracts/Contract.sol Indoaset 0x8e09fe761f4eee5dac56024cc5ef9174231e5f1b
```
Addresses.csv contains addresses of the contracts in examples folder.

## Sample Output
```
Calculating Slots
owner 0
newOwner 1
symbol 2
name 3
decimals 4
_totalSupply 5
balances 6
allowed 7


################ State Variables ################
['owner', 'address', '0x00000000000000000000000020b767115d0e2a23ca52ae3d7b87af61d4af5943', 20]
['newOwner', 'address', '0x0000000000000000000000000000000000000000000000000000000000000000', 20]
['symbol', 'string', '1ai', 32]
['name', 'string', 'Indoaset', 32]
['decimals', 'uint8', 18, 1]
['_totalSupply', 'uint', 20000000000000000000000000000, 32]
['balances:key:0x0358C107D0064d72Aa9040f7B6DAb92250C164F4', 'uint', 19998000000000000000000000000, 32]
['balances:key:0x0358c107d0064d72aa9040f7b6dab92250c164f4', 'uint', 19998000000000000000000000000, 32]
['balances:key:0x07CFcbEC279F57DEC79D0846815E0CCE682F7747', 'uint', 2000000000000000000000000, 32]

```

