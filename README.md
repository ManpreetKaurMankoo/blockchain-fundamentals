# blockchain-fundamentals, Solidity, Smart Contracts:

===================================== Lesson 0: Blockchain Basics ================================

Blockchains:
They are detereministic systems by design. Which means they themselves can't interact with the real world data and events. They don't know what the value of an Ethereum is, they don't know what random nos are, they don't know the temperature, they don't know any of this information. These blockchains also can't do any external computations. This is why blockchain are deterministic by design. This is so that all the nodes can reach consensus. If we start adding variable data, or random data or values that return from an API call, different nodes can get different results and they would never be able to reach a consensus.
Find more on this.


Smart Contracts:
Smart Contracts are a set of instructions executed in a decentralized manner without the need for a centralized or third party intermediary.
They come to life on blockchain or smart contract platforms like Ethereum.
They control the execution of agreements/transactions on top of blockchains.

Smart Contracts are similar to traditional contracts or agreements except that they are written in code and embodied and executed on decentralized blockchain platforms like Ethereum.

Once they are deployed on a decentralized blockchain, it cannot be altered (immutable), automatically executes, everyone sees the terms of agreement (transparent). 

They are: Immutable (terms of the contract cannot be changed by anyone - i.e. can't be hacked, manipulated or cant commit fraud), Decentralized (executed by a decentralized collectve - i.e. no one person/entity can change anything), Transparent (everyone on the chain will be notified in case anybody tries to change the terms of the contract)

Smart contracts is a tool that fixes the fundamental problem of promises/trust being broken by parties. This tool is what blockchain was built for.

Value of smart contracts:
They create trust minimized agreements - i.e they give rise to unbreakable promises. - Reduces counterparty risk Additionally, they give rise to speed, efficiency and transparency.

Ethereum protocol:
Bitcoin protocol and Ethereum protocol diff: Latter has smart contracts

Find more on Ethereum protocol:


Issue with blockchains: The Oracle problem.
They are intentionally walled off i.e. they cannot interact with and can't read or listen to data from the real world. This is known as the Oracle Problem.
But for the smart contracts to get executed, they would need external data and external computation. Hence, Blockchain Oracles come into picture.


Blockchain Oracle:
Any device that interacts with the off-chain world to provide external data or computation to smart contracts. However, if we want our applications to remain truly decentralized, we can't work with a single oracle or a single data provider or a single source that's running these external computations. So we need a decentralized Oracle Network similar to a decentralized blockchain network. i.e. On-chain logic as well as off-chain data and computation would also be decentralized. This gives rise to Hybrid smart contracts. This is also where Chainlink comes into picture.


Hybrid Smart Contracts:
Hybrid Smart Contracts = On-chain logic + Off-chain data and computation
                       = On-chain + Offchain agreements


Chainlink protocol:
It is a modular decentralized Oracle Network that can bring both external data as well as external computation into our smart contracts to make sure they are decentralized end-to-end while giving them the feature richness that we need for our agreements.
Chainlink is blockchain agnostic. So, it will work on Avalanche, Polygon, Solana, Phatom, Harmony, etc.

A no. of different blockchains or smart contract platforms have come to light, such as Avalanche, Polygon, Phantom, Harmony, etc.
Most blockhains are compatible with Ethereum type smart contracts.


Smart contract platform and blockchain are used interchangeably.

L2 layer: Solves scalability issues


DApps:
DApp = Decentralized Application = Decentralized Protocol = Smart contract
A DApp is usually a combination of many smart contracts.

Web1: The permissionless open sourced web with static content.
Web2: The permissioned web with dynamic content where companies run your agreements on their servers.
Web3: The permissionless web with dynamic content where decentralized censorship resistant networks run your agreement and your code. It is generally accompanied by the idea that users own the protocols that they work with and its an ownership economy, instead of being solely the product.


Decentralized Exchanges: (Decentralized Finance) - To prevent farudulent market manipulation
1. One such exchange is Uniswap: You can swap ERC20 tokens


DAOs: Decentralized Autonomous Organisations: They are groups governed completely decentralized by smart contracts on chain.

NFTs: Non Fungible Tokens - Digital Art or unique asset - 

Add the points in gmail draft - hierarchy of blockchain, blockchain platform, ethereum blockchain platform, ethereum protocol, etc.

----------------------------------
First transaction:
Done: 0.25 ETH

Transaction fee is the fee paid to the node executing the transaction (for the nodes to keep going - to keep validating the transactions)

Transaction fee = Gas Price * Gas used in ETH = (Block Base Fee Per Gas + MaxPriorityFee Per Gas) * Gas used
                = 21000 * 0.000000002500000007
                = 0.000052500000147

Base Fee = Minimum gas price to send our transaction.
Max Fee = Maximum gas fee that we are willing to pay for a transaction.
Max Priority Fee = Max Gas price we are willing to pay + Max tip that we are willing to give miners.

So, the one who sent 0.25 ETH, also paid 0.000052500000147 ETH to a blockchain node, to a validator, on this seploia ethereum testnet.
The calculation of this transaction fee may vary from blockchain to blockchain. For most EVM chains, this is the most simple algorithm.
The amount of gas a person choose to spend can be different depedning on how many people are making transactions with the blockchain. The more people are making transactions at the same time, the more expensive the gas costs are going to be. If more people are sending transactions at the same time, it means there is not going to be enough space for everyone's transactions to get through. So inorder to throttle that, they increase the gas price. Nodes get paid to for mining blocks.

EIP1559: Gas model working used in Ethereum


How do blockchains work?
Hash: A unique fixed length string meant to identify a piece of data. They are created by placing said data into a hash function.
Ethereum uses keccak256 for its hashing algorithm.

Hashing alogrithm:
A function that computers data into a unique hash.

Data:
Hash:

Block: A list of transactions mined together. It is basically a collection of block, transaction, previous hash to create to this unique hash for this block.

Block:
Nonce:
Data:
Hash:

Mining: Computationally intensive process of finding the solution to the 'blockchain' problem - by the miners

Blockchain:

Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Data:             Data:               Data:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:

Genesis block: First block in the blockchain where the previous hash points to a hash which does not actually exist.
So, here, Block, Nonce, Data and Prev hash all go through the hashing algorithm in the blockchain to arrive at Hash.

If somebody tries to change the data on a block, the solution to the problem calculated would be a mismatch when the change is done. Also, this mismatch will result in mismatches across all the blocks that are after this block in which the change was done. Hence, it is very difficult to change any data on a blockchain. (Immutable)


If I am the one who controls the blockchain and I have to change something in past on the blockchain (though it's very hard), I will go back and remine/rehash/redo all the blocks in the chain even if it is computationally expensive. This is where the distributed or decentralized nature of the blockchain makes it really powerful.

Distributed:

A no of different peers who are running the blockchain technology - they are all weighted equally - each one of these peers/nodes/entities running a blockchain has the exact same power as anybody else. So the way that we can tell very easily which blockchain is correct or which ones are correct is by looking at the last hash or by looking at where we are in the blockchain. (Decentralized). All these independent nodes running this blockchain, they are all matched up, its easy for their nodes to look at each other and say we are all matched up.

Peer A:
Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Data:             Data:               Data:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:

Peer B:
Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Data:             Data:               Data:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:

Peer C:
Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Data:             Data:               Data:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:


Now, let's say a node/peer say Peer A changed something on the blockchain at its end and even mined quickly to the last block - so that they have a valid blockchain. But their last hash on the blockchain will be different from the ones that other peers have. Majority rules in the blockchain.

Tokens:
Peer A:
Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Tx:               Tx:                 Tx:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:

Peer B:
Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Tx:               Tx:                 Tx:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:

Peer C:
Block:            Block:              Block:
Nonce:            Nonce:              Nonce:
Tx:               Tx:                 Tx:
Prev:             Prev:               Prev:
Hash:             Hash:               Hash:


Now in actual blockchain, instead of random data in this data/transaction section, there will be Solidity code and finding ways to interact with different blocks and different protocols that are on chain or different smart contracts.


Signing transactions:
Private key: Only known to the key holder, it's used to sign transactions.

Public key:
Ethereum and bitcon both use Elliptic Curve Digital Signature Algorithm to create the public key using hashing + other things.
So when we create the private key, the public key gets generated.

It is derived from our private key. Anyone can see it and use it to verify that a transaction came from us.

Private key is used to digitally sign the transactions. And people can then verify them using the public key.

How Elliptic Curve Digital Signature Algorithm works is, it can create the message signature with our private key but somebody else can't derive our private key from the message signature.

Sign=>
Message:
Private key:
	Sign
Message Signature:

Verify=>
Message:
Public key:
Signature (or Message Signature): 
	Verify


Using the public key, anybody can verify that the signature is ours.

Demonstrating the above in the form of a transaction:
1. We can sign the digital transaction using our private key
Sign=>
Message:
$:		From: 				To: 				
Private key:
	Sign
Message Signature:

2. Anybody can very the transaction using our public key.
Verify=>
Message:
$:		From: 				To: 
Signature:
	Verify

Signing transactions:
A one way process. Someone with a private key signs a transaction by their private key being hashed with their transaction data. Anyone can then verify this transaction hash with our public key.

Our address is derviced from our public key

Our private Key creates public key which in turn creates address key
Private Key ||| > Public Key > Address

Secret phrase >> Private Key ||| > Public Key > Address


==================================== High level blockchain fundamentals ===========================


Blockchain can be considered as a decentralized database and ethereum can be considered the same but has one more feature of doing computation.

Consensus, Proof of work, Proof of stake:
Proof of work and proof of stake fall under the umbrealla of consensus.
The mining that we did was example of proof of work.

Consensus: It is the mechanism used to agree on the state of a blockchain. (One mismatch, does not match with others, will get thrown out. This is a part of the consensus mechanism).

Proof of work:

Proof of stake:


Layer 1: Refers to any base layer blockchain implementation. For eg: Blockchain, Avalanche, Ethereum
Layer 2: Any application built on top of layer 1. For eg: Chainlink, Arbitrom, Optimism

Arbitrom and Optimism are known as Roll-ups and the roll up their transactions into a layer one like Ethereum.
They solve some of the scalability issues by being another blockchain that people can make transactions on, still on kind of this base ethereum layer.
They are different from side chains because side chains derive their security from their own protocols. Roll ups derive their security from base layers.

Sharding and roll ups are solutions to scalability issues on layer 1.

================================= Lesson 1: CODING: REMIX ====================================
Deploying a smart contract on a blockchain is done by making a transaction - which costs gas
Calling any function of smart contract is done by making a transaction - which costs gas

Just setting a variable or a function to private isn't a good way to hide what the value actually is there. Everything on these EVM chains is actually public data. More on storage and visibility later on.

Function and variable visibility:
public: Visible externally and internally. Visible to an external contract and can be called by it
private: Only visible in the current contract
external: Only visible externally (only for functions, means not for variables). It means another function inside the contract couldn't call an external function.
internal: Only visible internally - means, only the current contract and its child contract can call the function


Every time we update the state of the blockchain, it is going to cost us gas. The store() function is not reading but updating something. i.e. it is changing the state of the blockchain, so we have to send a transaction.

  function store(uint256 _favouriteNumber) public {
    favouriteNumber = _favouriteNumber;
  }

View function:
A function marked as view means we are just going to read state from the blockchain, so we don't need to send a transaction.

  function store(uint256 _favouriteNumber) public {
  	favouriteNumber = _favouriteNumber;
  }

    function retrieve() public view returns(uint256)  {
    	return favouriteNumber;
  }

 The above is an example of view function.


 So, if we have view function, it disallows any modification of the state. Meaning, we cannot have the below given line where we are updating the favouriteNumber:
     function retrieve() public view returns(uint256)  {
         favouriteNumber = _favouriteNumber + 1;
    	return favouriteNumber;
  }

Pure function:
A function marked as pure disallows updating state and they disallow even reading from state or storage.

The variable favouriteNumber below is known as storage variable because it is stored in a place called storage. It is implicitly converted to a storage variable since it is added in the state context i.e. outside of the fucntion, inside the contract.

contract SimpleStorage {
  uint256 public favouriteNumber;

  function store(uint256 _favouriteNumber) public {
    favouriteNumber = _favouriteNumber;
  }
}

So, because of this, the below won't be allowed:
    function retrieve() public pure returns(uint256)  {
    	return favouriteNumber;
  }

favouriteNumber is a storage variable and pure function disallows reading from state or storage. But the below is allowed. Below is an example of pure function:

    function retrieve() public view returns(uint256)  {
    	return 7;
  }

So for a view and pure function, we don't need to spend gas because they don't change state.

So, in Remix IDE, buttons in blue represents view or pure functions that we can call without having to send transactions.

But, calling a view or pure function actually does cost gas only when a gas cost transaction is calling it.

contract SimpleStorage {
  uint256 public favouriteNumber;

  function store(uint256 _favouriteNumber) public {
    favouriteNumber = _favouriteNumber;
    retrieve(); // This store function is calling retrieve function which is pure function. But since store function will cost gas, calling retrieve function will also cost gas.
  }

  function retrieve() public pure returns(uint256)  {
    	return favouriteNumber;
  }
}

----------------------
In solidity, we can create our own type using struct.

  struct Person {
    uint256 favouriteNumber;
    string name;
  }

Here, we are creating a type Person. Each person will have a favouriteNumber and a name.
Then, we can create a variable of type Person.

struct Person {
    uint256 favouriteNumber;
    string name;
}

Person public myPerson = Person(7, "Tim");

or

Person public myPerson = Person({favouriteNumber: 7, name: "Tim"});

Instead of adding details of people one by one, we can do this - we can declare a dynamic array and create a add function to add values to the array.

Person[] public listOfPeople;

function addPerson(string memory _name, uint56 _favouritenumber) public {
	
}

Arrays come built in with a function called push which allows us to add elements or add person here to our list of Person array.
So when we deploy the contract, and click on the listOfPeople blue button, we will have to provide the index first to retrieve the required value.

We can push to the array in two ways:
Person memory myPerson = Person(_favouriteNumber, _name);
listOfPeople.push(myPerson);

or

listOfPeople.push(Person(_favouriteNumber, _name));

ChatGPT:
Phind: AI which searches all the relevant links and gives the answer based on the sereach on those links.
Github discussions:
Stack exchange ethereum: For asking technical questions about Ethereum
Peeranha: Decentralized stack exchange

===================================== Lesson 2: Memory, storage, call data intro  ================================

There are 6 places where we can store data in solidity:
EVM can access and store information in 6 places:
1. Stack
2. Memory
3. Storage
4. Calldata
5. Code
6. Logs

Calldata and memory are temporary variables. Temporary variable means it exist only for the duration of the function call in which it is used.

Calldata: Is temporary variables that cannot be modified. A calldata variable cannot be changed or manipulated/modified.
function addPerson(string calldata _name, uint56 _favouritenumber) public {
	_name = "cat"; // Not alllowed
}

Memory: Is temporary variavles that can be modified. A memory variable can be changed or manipulated/modified.
function addPerson(string memory _name, uint56 _favouritenumber) public {
	_name = "cat"; // Allowed
}

If a variable type is calldata or memory (for eg _name above), it can be accessed only once. Because it will exist only for that short duration - i.e. when it is called - i.e. only once.

Inside of functions, most variables default to memory variables. Strings are a special type in Solidity, so we have to specify whether it is memory or calldata, it has to do with how arrays work in memory.

Storage: Is permanent variables that cannot be modified

We can make the variables in the function call as only calldata, memory or storage.

We cannot give these variable types for all variables.
Array, structs, mapping are considered special types in solidity and the way memory management works under the hood makes it so that we have to put this memory keyword.
uint256 is known as a primitive type and solidity is smart enough to know where to put this variable number always under the hood.

A string is actually an array of bytes. So we need to put the memory keywords for _name which is an array (string). So, what about storage, can we give storage type to _name. No. Because solidity is smart enough to know that this variable is in a function and will last only within this function, so it is temporary and thus making it a storage (permanent variable) wont be allowed. So, we got to pick either memory or calldata.

So summary: Arrays, structs, mappings need to be given memory keyword. String is an array of bytes, so it needs to be given memory or calldata keyword.

===================================== Lesson 2: Basic Solidity Mappings ================================
mapping(string => uint256) public nameToFavouriteNumber; // If we want Chelsea's favourite number, we will put in Chelsea and in the output get Chelsea's favourite number due to this mapping and below logic:

function addPerson(string memory _name, uint56 _favouritenumber) public {
	nameToFavouriteNumber[_name] = _favouriteNumber;
}


===================================== Lesson 2: Deploying your first smart contract ================================


===================================== EVM ==============================================================
Whenever we compile the code, it compiles down to something called EVM. EVM is a standard for how to compile and how to deploy smart contracts to blockchain (that is EVM compatible).
Some egs of EVM compatible blockchains and layer2s: Ethereum, Polygon, Arbitrum, Optimism, ZK Sync, ...

Whenever we hit compile in our smart contracts, it actually compiles our solidity code down to EVM compatible byte code or machine readable code.

Code till lesson 2:

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract SimpleStorage {
  uint256 myFavouriteNumber;

  mapping(string => uint256) public nameToFavouriteNumber;

  function store(uint256 _favouriteNumber) public {
    myFavouriteNumber = _favouriteNumber;
  }

  struct Person {
    uint256 favouriteNumber;
    string name;
  }

  Person public myPerson = Person({favouriteNumber: 7, name: "Tim"}); // or Person public myPerson = Person(7, "Tim");

  Person[] public listOfPeople;

  function retrieve() public view returns(uint256) {
    return myFavouriteNumber;
  }

  function retrieve1() public pure returns(uint256) {
    return 7;
  }

  function addPerson(string memory _name, uint56 _favouriteNumber) public {
    // Person memory myPerson = Person(_favouriteNumber, _name);
    // listOfPeople.push(myPerson);

    listOfPeople.push(Person(_favouriteNumber, _name));
    nameToFavouriteNumber[_name] = _favouriteNumber;

  }
}

===================================== Lesson 3: Remix Sorage Factory ================================
Contracts can deploy other contracts and can also interact with them.
Contracts interacting with each other seamlessly and permissionlessly is a feature of smart contracts and blockchain development that is absolutely essential and crucial and one of the reasons why blockchain development is so powerful. The ability for contracts to interact with each other seamlessly is something known as composability. Smart contracts are composable because they can easily interact with each other. This becomes even more impt in case of DeFi where incredibly complicated financial products and intruments interact with each other seamlessly because they are all using the same smart contract interface. 

===================================== Lesson 3: Setup ================================
In order to deploy a contract from another contract, the contract that is deploying should know about the other contract. this can be done by putting both the contracts in one file.
We can have multiple contracts in a same file. But while deploying, we will have to take care and select the right contract for deploying. Also, it is not a best practice to keep more than one contract in one file.

===================================== Lesson 3: Deploying a contract from a contract ================================
We will have a function within contract 1 to deploy contract 2 but we are going to save it to a storage or state variable like 
uint256 public favouriteNumber;
// type visibility variable name

SimpleStorage public simpleStorage;
// contract type visibility variable name


function createSimpleStorageContract() public {
	simpleStorage = new SimpleStorage();
}

So, with this new keyword, Solidity knows to deploy a contract.

We deploy the contract 1 (which will deploy contract 2). Then, when we click on the 'createSimpleStorageContract' function orange button (for creating contract 2), then contract 2 deployed. When we click on the blue button for variable simpleStorage, it gives us the address of contract 2.

Note: A red button indicates it is payable button.

===================================== Lesson 3: Imports ================================
For better organization:

pragma solidity ^0.8.18;

import "./SimpleStorage.sol";

But advanced import (named import), which is recommended because lets say contract 2 has more than one contract under it. So in case we want to import only specific file, then advanced import to be used.
import {SimpleStorage} from "./SimpleStorage.sol";
import {SimpleStorage2} from "./SimpleStorage.sol";

===================================== Lesson 3: Interacting with contracts ABI ================================
ABI - Application binary Interface
To interact with a contract, we always need two things:
- Address
- ABI (we actually need a function selector)

To interact with other contracts from another contract:

function sfStore(uint256 _indexSimpleStorage, uint256 _newSimpleStorageNumber) public {
	SimpleStorage mySimpleStorage = listOfSimpleStorageContracts[_indexSimpleStorage];
	mySimpleStorage.store(_newSimpleStorageNumber); // store here is the method from contract 2
}

===================================== Lesson 3: Inheritance ================================
First, named import needed for inheritance. Then is <contract>

import {SimpleStorage} from "./SimpleStorage.sol";

contract AddFiveSimpleStorage is SimpleStorage {
	
}

To override a function of the inherited contract, we need override and virtual. Overriding function should have override and overridden function should have virtual.

So, overriding function:
function store(uint256 _newNumber) public override {
		myFavouriteNumber = _newNumber + 5;
}

overridden function:
function store(uint256 _favouriteNumber) public virtual {
	myFavouriteNumber = _favouriteNumber;
}

===================================== Lesson 4: Remix Fund Me (Advanced Solidity features) ================================

===================================== Lesson 4: Setup ================================

// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    function fund() public {

    }

    function withdraw() public {

    }
}

===================================== Lesson 4: Sending ETH through a function ================================

// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?

    }

    function withdraw() public {

    }
}


Solodity has a number of globally available keywords and functions - can be found in solidity documentation.
One of them is msg.value - which is - The no. of Wei sent with the msg.

// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?
        require(msg.value>1e18, "Didn't send enough ETH"); // 1e18 = 1 ETH = 1000000000000000000 = 1 * 10 ** 18

    }

    function withdraw() public {

    }
}

===================================== Lesson 4: Reverts ================================

What is a revert?: Undo any actions that have been done, and send the remaining gas back.

If the transaction fail, the gas that was spent will be refunded. So, in the below code, myValue = 1 will be incremented to 1+2 = 3 and the next require line will be executed but it will fail if the fund being sent is less than or equal to 1 ETH. But even though the transaction didn't go through, the gas will be spent. But it will be refunded.

// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    uint256 public myValue = 1;

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?
        myValue = myValue +2;
        require(msg.value>1e18, "Didn't send enough ETH"); // 1e18 = 1 ETH = 1000000000000000000 = 1 * 10 ** 18

        // What is a revert
        // Undo any actions that have been done, and send the remaining gas back 
    }

    function withdraw() public {

    }
}


Every single transaction that we send, will have these fields:
Nonce: Tx count for the account
Gas Price: Price per unit of gas (in wei)
Gas Limit: Max gas that this transaction can use
To: Address that the Tx is sent to
Value: Amount of Wei to send
Data: What to send to the To address
v, r, s: Components of a Tx signature

For a function call, we can also populate the Wei that we want to send. So we can call a function and send a value (in Ether, Gwei or Wei) at the same time.

===================================== Lesson 4: Getting real world price data (Chainlink) ================================
docs.chain.link

In the below code, msg.value is in ETH or Wei and minimumUsd is in $. So how do we convert the amount of Ethereum to its price in USD. This is where oracles and chainlinks come into play. The dollar price of an asset like Ethereum is something that we have assigned to Ethereum outside of the blockchain in the real world.

// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    uint256 public minimumUsd = 5;

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?
        require(msg.value > minimumUsd, "Didn't send enough ETH"); // But msg.value is in ETH or Wei and minimumUsd is in $

        // What is a revert
        // Undo any actions that have been done, and send the remaining gas back 
    }

    function withdraw() public {

    }
}

So in order to get the abstract concept of the price of the native cryptocurrency of the blockchain working with, so we need to use a decentralized Oracle Network or something called as oracle to get this price.

They are detereministic systems by design. Which means they themselves can't interact with the real world data and events. They don't know what the value of an Ethereum is, they don't know what random nos are, they don't know the temperature, they don't know any of this information. These blockchains also can't do any external computations. This is why blockchain are deterministic by design. This is so that all the nodes can reach consensus. If we start adding variable data, or random data or values that return from an API call, different nodes can get different results and they would never be able to reach a consensus. This is known as the smart contract connectivity problem or the Oracle problem.
But we want our smart contracts to be able to do traditional payments. And traditional payments need data and they need to interact with the real world. This is where Chainlinks and blockchain Oracle come into place.

Blockchain Oracle:
It can be any device that interacts with the offchain world to provide external data or computation to smart contracts. However, if we are using a centralized oracle, we are reintroducing a point of failure for which we have done all this work to make our logic layer decentralized. We are ruining the entire purpose of building a smart contract. So we don't want to get data or do external computation through centralized nodes. Chainlink is the solution here.

Chainlink:
It is a Decentralized Oracle Network for bringing data and external computation into our smart contracts. This gives rise to Hybrid Smart Contracts which combine on-chain and off-chain to make incredibly feature-rich powerful applications. Chainlink is a modular decentralized network that can be customized to deliver any data or do any external computation.

Features of Chainlink:
1. Chainlink Data Feeds:
They are powering over $50 billion in the DeFi world.

How they work:

A network of chainlink nodes gets data from different exchanges and data providers and bring that data through a network of decentralized chainlink nodes. The chainlink nodes use a median to find out what the actual price of the asset is and then deliver that in a single transaction to what's called a Reference Contract or Price Feed Contract or Data Contract on chain that other Smart Contracts can use and then those Smart Contracts use that pricing information to power their DeFi application.

2. Chainlink VRF (Verifiable Randomness Function):
Randomness can be manipulated in blockchain (more on this later). [Malicious RNG (Random Number Generators) Operators are a risk].
Blockchains are deterministic systems which means they can't have randomness. If you can determine what a random number is, it really isn't random. So we need a provably random number by looking outside of the blockchain and oracles are perfectly positioned to do exactly that. Chainlink VRF fucntion is a way to get provably random number into our smart contract to guarantee fairness and to guarantee randomness of applications.


3. Chainlink Keepers:
Decentralized Event-Driven Execution
In order to kick off some type of transaction, somebody needs to spend the gas and somebody needs to hit the go button or hit the transact button or hit the send button. This is obviously a centralized vector. If you have a decentalized application that needs to run at specific times or after specific events are triggered, chainlink keeprs are the solution to this.
Chainlink keepers are chain link nodes that listen to a registration contract for different events that you specify to fire, may be you say every 10 mins you want to do something etc. The chainlink nodes constantly listen for these triggers to happen and check the different contracts for these triggers. Once a trigger returns true, the chainlink nodes will then perform whatever action that you tell the chainlink nodes to do.

4. End-to-end reliability:
It is the promise of smart contracts


===================================== Lesson 4: Interfaces ================================
So, in the above code, msg.value is in ETH or Wei and minimumUsd is in $. So we need convert the amount of Ethereum to its price in USD. We will use chainlink data feed.

// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    uint256 public minimumUsd = 5;

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?
        require(msg.value > minimumUsd, "Didn't send enough ETH"); // But msg.value is in ETH or Wei and minimumUsd is in $
    }

    function withdraw() public {

    }

    function getPrice() public {
    	// We need address and ABI

    }

    function getConversionRate() public {

    }

    function getVersion() public view returns(uint256) {
		return AggregatorV3Interface(0x694jhdjkSGgjh786786).version();
	}
}

A common way that people use to interact with other contracts outside of their projects is - they get the interface of that contract using the interface keyword, they compile it and the compiler actually gives us the ABI and then you just wrap an address around with that interface keyword and you can call any function at that address.


===================================== Lesson 4: Importing from npm/GitHub ================================
Import a contract from outside of our project: import directly from GitHub:

import {AggregatorV3Interface} from "@chainlink/contracts/src/v0.8/interfaces/AggregatorV3Interface.sol";


===================================== Lesson 4: Getting prices from chainlink ================================
// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    uint256 public minimumUsd = 5e18; // Since getConversionRate() returns a value iwth 18 decimal places, we need to update our minimum USD to say 5 * (10 ** 18) or 5 * 1e18 or 5e18

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?
        require(getConversionRate(msg.value) >= minimumUsd, "Didn't send enough ETH"); // But msg.value is in ETH or Wei and minimumUsd is in $
    }

    function withdraw() public {

    }

    function getPrice() public view returns (uint256) { // view since reading from storage
    	// We need address and ABI

    	AggregatorV3Interface priceFeed = AggregatorV3Interface(0x694jhdjkSGgjh786786);
    	(, int256 price, , , ) = priceFeed.latestRoundData(); // since latestRoundData() returns a bunch of things but we are focused on only one - price. This price is going to 

    	// represent the price of ETH in USD and it will look like this - 200000000000. There are no decimals in Solidity, so this actually should have been 2000.00000000
    	// ETH has 18 decimal places in WEI, this above number has 8 decimal places in place. So the diff is 10. So,

    	return uint256(price * 1e10); // Returns value of Ethereum in terms of USD as a unit256. Now we have to convert our msg.value in terms of dollars using our getPrice() //function. To do that, we will use our getConversionRate() function.

    }

    function getConversionRate(uint256 ethAmount) public view returns(uint256) {
    	uint256 ethPrice = getPrice();
    	uint256 ethAmountInUsd = (ethPrice * ethAmount) / 1e18;
    	return ethAmountInUsd;
    }

    function getVersion() public view returns(uint256) {
		return AggregatorV3Interface(0x694jhdjkSGgjh786786).version();
	}
}


===================================== Lesson 4: msg.sender ================================

We need to maintain a list of senders who are/will be sending the money.
We can also create a mapping of addresses to lookup how much mney each sender has sent. 


// Get fund from users
// Withdraw funds to users
// Set a minimum funding value in USD

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

contract FundMe {

    uint256 public minimumUsd = 5e18; // Since getConversionRate() returns a value iwth 18 decimal places, we need to update our minimum USD to say 5 * (10 ** 18) or 5 * 1e18 or 5e18

    address[] public funders;
    mapping(address => uint256) public addressToamountFunded; // or mapping(address funder => uint256 amountFunded) public addressToAmountFunded;

    function fund() public payable {
        // Allow users to send money
        // Have a minimum $ sent
        // 1. How do we send ETH to this contract?
        require(getConversionRate(msg.value) >= minimumUsd, "Didn't send enough ETH"); // But msg.value is in ETH or Wei and minimumUsd is in $

        funders.push(msg.sender); // msg.sender is another global variable that can be used in Solidity which refers to whoever calls this function, the sender of the transaction to this contract.

        addressToAmountFunded[msg.sender] = addressToAmountFunded[msg.sender] + msg.value;
    }

    function withdraw() public {

    }

    function getPrice() public view returns (uint256) { // view since reading from storage
    	// We need address and ABI

    	AggregatorV3Interface priceFeed = AggregatorV3Interface(0x694jhdjkSGgjh786786);
    	(, int256 price, , , ) = priceFeed.latestRoundData(); // since latestRoundData() returns a bunch of things but we are focused on only one - price. This price is going to 

    	// represent the price of ETH in USD and it will look like this - 200000000000. There are no decimals in Solidity, so this actually should have been 2000.00000000
    	// ETH has 18 decimal places in WEI, this above number has 8 decimal places in place. So the diff is 10. So,

    	return uint256(price * 1e10); // Returns value of Ethereum in terms of USD as a unit256. Now we have to convert our msg.value in terms of dollars using our getPrice() //function. To do that, we will use our getConversionRate() function.

    }

    function getConversionRate(uint256 ethAmount) public view returns(uint256) {
    	uint256 ethPrice = getPrice();
    	uint256 ethAmountInUsd = (ethPrice * ethAmount) / 1e18;
    	return ethAmountInUsd;
    }

    function getVersion() public view returns(uint256) {
		return AggregatorV3Interface(0x694jhdjkSGgjh786786).version();
	}
}

===================================== Lesson 4: Library ================================

solidity-by-example.org/library

Libraries are similar to contracts, but you can't declare any state variable and you can't send ether.
A library is embedded into the function if all library functions are internal.
Otherwise the library must be deployed and then linked before the contract is deployed.

---------------PriceConvertor.sol-------------------

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

import {AggregatorV3Interface} from "@chainlink/contracts/src/v0.8/interfaces/AggregatorV3Interface.sol";

library PriceConvertor {

    function getPrice() internal view returns (uint256) { // view since reading from storage
    	// We need address and ABI

    	AggregatorV3Interface priceFeed = AggregatorV3Interface(0x694jhdjkSGgjh786786);
    	(, int256 price, , , ) = priceFeed.latestRoundData(); // since latestRoundData() returns a bunch of things but we are focused on only one - price. This price is going to 

    	// represent the price of ETH in USD and it will look like this - 200000000000. There are no decimals in Solidity, so this actually should have been 2000.00000000
    	// ETH has 18 decimal places in WEI, this above number has 8 decimal places in place. So the diff is 10. So,

    	return uint256(price * 1e10); // Returns value of Ethereum in terms of USD as a unit256. Now we have to convert our msg.value in terms of dollars using our getPrice() //function. To do that, we will use our getConversionRate() function.

    }

    function getConversionRate(uint256 ethAmount) internal view returns(uint256) {
    	uint256 ethPrice = getPrice();
    	uint256 ethAmountInUsd = (ethPrice * ethAmount) / 1e18;
    	return ethAmountInUsd;
    }

    function getVersion() internal view returns(uint256) {
		return AggregatorV3Interface(0x694jhdjkSGgjh786786).version();
	}
}



---------------FundMe.sol------------------

//SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

import {PriceConvertor} from "./PriceConvertor.sol";

contract FundMe {

	using PriceConvertor for uint256;

    uint256 public minimumUsd = 5e18; // To attach the functions in PriceConvertor library to all uint256s 

    address[] public funders;
    mapping(address => uint256) public addressToamountFunded;

    function fund() public payable {
    	// msg.value.getConversionRate // Here msg.value of type uint256 will be passed as the first parameter to the getConversionRate function, because of using Priceconvertor for uint256 above, so the next line will be

        require(msg.value.getConversionRate() >= minimumUsd, "Didn't send enough ETH");

        funders.push(msg.sender);

        addressToAmountFunded[msg.sender] = addressToAmountFunded[msg.sender] + msg.value;
    }

    function withdraw() public {}

 }


===================================== Lesson 4: SafeMath ================================
SafeMath, overflow, checking, and the "unchecked" keyword

Before 0.8 version, SafeMath.sol library was used extensively.
unchecked: If upper limit is passed, it will restart from the lower number --> This is known as overflow - Shift

After version 0.8, they added this check, if it overflows, it won't allow to add further and would give an error on that transaction.

We can revert back to the unchecked version (in solidity versions 0.8 or greater), by:
function add() public {
	unchecked {bigNumber = bugNumber + 1};
}

===================================== Lesson 4: For Loop ================================


for(/* starting index, ending index, step amount */)

for(uint256 fundeRIndex = 0; funderIndex < funders.length, funderIndex++) {
	
}

There are 3 different ways to send Ethereum or tokens from different contracts to each other:
1. Transfer
2. Send
3. Call

payable(msg.sender).transfer(address(this).balance); // transfer, issue with this: transfer is capped at 2300 gas, if more gas used - then gives error and reverts the transaction.

===================================== Lesson 4: Withdraw ================================

solidity-by-example.org/sending-ether

bool sendSuccess = payable(msg.sender).send(address(this).balance); // send is capped at 2300 gas, if more is used, then will not give an error but return a boolean whether or //not it was successful.
require(sendSuccess, "Send failed"); // adding this require will revert

// Call is not capped for gas, so forwards all gas, returns bool
(bool callSuccess, bytes memory dataReturned) = payable(msg.sender).call{value: address(this).balance}(""); // this call function returns 2 variables

But we dont care about the dataReturned, so:
(bool callSuccess, ) = payable(msg.sender).call{value: address(this).balance}("");
require(callSuccess, "Call failed");


===================================== Lesson 4: Constructor ================================
Only the owner of the contract should be able to withdraw the money. So, how do we set the contract up so that the withdraw function can only be called by the owner of the contract. We want to set this contract such that when the contract gets deployed, the owner gets assigned to this contract. We assign some address to the onwer and then we add some parameters so that withdraw can only be called by that address. So, we can set up some function say callMeRightAway() and when we deploy the contarct, we would just immeditaely call the callMeRightAway() fucntion which will set us up as the owner. However, that would take 2 transactions. This is where constructor comes into play.

constructor is a keyword and special function which is immediately called when we deploy our smart contract. We don't even need to use the function keyword for it. This constrcutor will be called in exact same transaction that is used to deploy our contract. We can set up the address of the owner of the contract in this constructor.

address public owner;

constructor() {
	owner = msg.sender;	// msg.sender here being the caller which will be the deployer of the contract
}

Now that the owner is set up, we can now modify our withdraw() function so that only the owner can call this function. So, we can use the require function:

function withdraw() public {
	require(msg.sender == owner, "Must be owner");
}

But, let's say we have a lot of functions that should only be called by owner. In that case, we would have to put the require check in each such function. To avoid this,
modifiers will come into place. modifier is going to allow us to create a keyword that we can put right in the function declaration (of withdraw() function here) to add some functionality very quickly and easily to any function.


constructor() {
	owner = msg.sender;	// msg.sender here being the caller which will be the deployer of the contract
}

function withdraw() public onlyOwner {
	require(msg.sender == owner, "Must be owner")
}

modifier onlyOwner(){
	require(msg.sender == owner, "Must be owner");
	_;
}

So, it going to execute what's in the modifier first i.e. require() and then _ says do anything else that you want to do after this, which will be returning back to the withdraw() here.

If we had the _ before the require(), it would execute whatever is in withdraw() and then come to teh require() function.


===================================== Lesson 4: Advanced Solidity - Immutable & Constants ================================

If we have variables outside of a function that get set only one time and never changes, we can use some tools in Solidity to make them more gas efficient.

There are two keywords in Solidity that make it so that your variables cannot be changed: constant and immutable. The reason that these two save gas is instead of storing these variables inside of a storage space, we actually store them directly into the bytecode of the contract.

If we have a variable outside of a function that get set only one time and never changes, if it is assigned at compile time, we can assign the constant keyword:

uint256 public constant MINIMUM_USD = 5e18; // When constant is mentioned, the variable no longer takes up teh storage space and is much easier to read from.

View functions do have gas costs when called by a contract.

Another variable that we set only once: owner

If we have a variable that we set only once but outside of the same line that it is declared (like in owner variable's case), we can mark it as immutable.

address public immutable i_owner;

===================================== Lesson 4: Advanced Solidity - Custom errors  ================================

More gas optimizations:

Each of the error log in the require function needs to be stored individually as a String. Custom error come into place here. This says us a lot of gas as we don't have to store and emit this long string in the require function.

error NotOwner();

contract FundMe {
	
	modifier onlyOwner {
	// require(msg.sender == i_owner, "Sender is not owner"); // We can replace this with if and custom error

	if (msg.sender != i-owner) {
		revert NotOwner();
	}
	}
}

===================================== Lesson 4: Advanced Solidity - Receive & Fallback   ================================
Sometimes, people will try to interact with the contract takes Ethereum or the native blockchain token without actually going through the required function calls that are needed. For eg, user can send the contract money without calling the fund() function. However, if that happens, what will happen, will the fund() function get triggerred? No, it won't. We want to keep track of that funder but we would not have that person's information updated in this contract. Or later on if we want to give some rewards, but we wouldn't know about those funders. So what can we do in this case?

What happens when someone sends this contract ETH without calling the fund() function?

There is a way for when people send money to this contract or people call a function which does not exist for us to still trigger some code.
Two special functions in Solodity: receive() and fallback()

Receive function:
A contract can have at most one receive function declared using the receive() external payable (without the function keyword). This function cannot have arguments, cannot return anything and must have external visibility and payable state mutability. It can be virtual, can override and can have modifiers.

Fallback function:
A contract can have at most one fallback function, declared using either fallback() external [payable] or fallback(bytes calldata input) external [payable] returns (bytes memory output) (both without the function keyword). This function must have external visibility. It can be virtual, can override and can have modifiers.

If data is sent with a transaction and no function is specified (calldata transaction in remix), the transaction will default to the fallback function if tha fallback function exists.
If calldata is blank, it will trigger the receive function if it exists. If it does not exist, it will trigger the fallback function.
But if there is data in calldata that doesn't specify any of the other functions, it will trigger the fallback function if it exists. If it does not exist, it will give error.

Explainer from: https://solidity-by-example.org/fallback

Ether is sent to contract
	is msg.data (calldata) empty?
		/	          \
	 yes               no
	 /                   \
 receive()?              fallback()
   /     \                      /   \
 yes      no                  yes    no
 /          \                 /        \
receive()  fallback()    fallback()     error		


===================================== Lesson 5: AI Prompting & Forums ================================
===================================== Lesson 5: Introduction  ================================
===================================== Lesson 5: & Triage steps for this course  ================================
===================================== Lesson 5: Speedrun ethereum ***  ================================

Checkout speedrun ethereum and Scaffhold ETH after the course


===================================== Lesson 6: Foundry Simple Storage ================================
===================================== Lesson 6: Introduction ================================
Foundry:
It is a smart contract development toolchain/framework. It is completely Solidity based. So, it is the fastest to work with for smart contract development (HardHat is Javascript based, Brownie is Python based).
It manages your depdendencies, compiles your project, runs tests, deploys, and lets you interact with the chain from the command line and via the Solidity scripts.


Why Foundry?
It helps us to deploy our smart contracts, tets our smart contracts and interact with them in a much more progammatic way rather than we having manually to click around.

VS Code:
Ctrl + `: Opens and closes terminal
Cmd + k: Clears the terminal
Ctrl + W: Clears the most recent block of code you have written
Ctrl + U: Deletes the entire line
Cmd + Sft + P: view bar

===================================== Lesson 6: Foundry Install and Local Development Setup ================================

===================================== Lesson 6: Foundry Compile ================================
forge compile
===================================== Lesson 6: Deploying to a local blockchain (Anvil or Ganache) ================================
Anvil:
In Remix, we used Remix VM (Virtual Machine) to deploy our code. So, in Foundry, we want to do the same. Foundry comes with a built-in a virtual environment in the shell and if you run Anvil, then you get some output.

Ganache:
Ganache is a one click blockchain and it gives us an interface or an app to look at our transactions in an easier way. So download Ganache, if needed.

RPC URL:
Each of the network - Sepolia, etc - comes with a bunch of info: Name, RPC URL, Chain ID, Currency symbol, Block explorer URL

RPC URL is the actual https endpoint that we actually send the API calls to when we are sending transactions. So whenever you interact with Metamask and you send a transaction or you deploy a contract, you are actually making an API call to the RPC URL.


forge create:
Now that we have an endpoint and a private key (one of the dummy private keys of Anvil that is publicly available) to deploy to our own local blockchain be it Ganache or Anvil. There are 2 ways to deploy a contract:
1. Command line: forge create SimpleStorage --rpc-url http:127.0.0.1:8545 --interactive
2. Script for deploying: forge script:

Script:
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.18;

import {Script} from "forge-std/Script.sol";
import {SimpleStorage} from "../src/SimpleStorage.sol";

contract DeploySimpleStorage is Script {
    function run() external returns (SimpleStorage) {
        vm.startBroadcast(); // vm comes from Script.sol
        SimpleStorage simpleStorage = new SimpleStorage();
        vm.stopBroadcast();
        return simpleStorage;
    }
}

command:
forge script script/DeploySimpleStorage.s.sol // if rpc url not specified, it will automatically deploy it on some temp anvil address.

forge script script/DeploySimpleStorage.s.sol --rpc-url 127.0.0.1:8545 --broadcast --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80
for now we can't not give private key for forge script

cast --to-base 0x714c2 dec:

===================================== Lesson 6: ThirdWeb Deploy ================================

forge fmt: will format all the code - if we are working on another's code

===================================== Lesson 6: Summary ================================
forge --init: will give all the folders in the project

cast: Used for interacting with contracts that have already been deployed
anvil: Used to deploy a local blockchain similar to ganache
forge: forge create and forge script

===================================== Lesson 7: Foundry Fund Me ================================

===================================== Lesson 7: Introduction ================================



