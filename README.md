# moneylegos
Go Ethereum testnet with Proof of Authority consensus

# Dependencies
Go Ethereum
https://geth.ethereum.org/downloads/

# Network Setup
These are the following steps to configure this testnet up from scratch:

## Step 1: Set up Accounts for Two Nodes
* Input the following command: ./geth account new --datadir *yournodename*
* Enter and confirm a password to unlock this.
* <img width="578" alt="Screen Shot 2021-07-26 at 5 37 22 PM" src="https://user-images.githubusercontent.com/40152804/127062593-0542ae77-c3bc-463a-bf63-a814cb054e5e.png">
* Repeat this step with at least one other node using a different nodename.

## Step 2: Initialize the network using CLI
* Enter ./puppeth
* You could use any network name you like as long as it follows the naming convention specified by geth.
* <img width="583" alt="Screen Shot 2021-07-25 at 3 33 09 PM" src="https://user-images.githubusercontent.com/40152804/126911113-d4b2a16b-0c09-4fda-a5f0-9aad9437561b.png">

## Step 3: Network Configuration
* Select option 2 (Configure new genesis) for "What would you like to do?"
* Then select option 1 (Ceate new genesis from scratch) for another "What would you like to do?" prompt.
* Next, select option 2 (Clique - proof-of-authority) for consensus engine.
* This testnet was left with the default blocktime of 15 seconds.
* <img width="372" alt="Screen Shot 2021-07-25 at 4 57 11 PM" src="https://user-images.githubusercontent.com/40152804/126913272-63fcd56c-71b6-4529-af99-7dedbc2f7dc1.png">

## Step 4: More Network Configuration
* Select which of the accounts from step 1 are allowed to seal (once finished with selection, press enter on next "0x" prompt)
* Select which accounts from step 1 should be prefunded
* Precompiled-addresses do not need to be prefunded, so no was selected
* Specify your chain/network ID or choose random by not providing an ID (this information can be looked up later)
* <img width="570" alt="Screen Shot 2021-07-25 at 6 02 09 PM" src="https://user-images.githubusercontent.com/40152804/126914800-e91b5e19-bf62-466f-9eab-a93a1f473016.png">

## Step 5: Exporting Network Configurations
* Select option 2: "Manage existing genesis"
* Next, select option 2: "Export genesis configurations"
* Choose which folder you would like to save the genesis configuration in.
* <img width="567" alt="Screen Shot 2021-07-25 at 6 05 38 PM" src="https://user-images.githubusercontent.com/40152804/126914873-d7535323-5039-495c-9b57-757ebdc8e681.png">

## Step 6: Initialize Nodes
* Crtl-C puppeth
* Use the following command on both of your nodes: ./geth init yournetworkname.json --datadir *yournodename*
* This is what the output should look like:
* <img width="568" alt="Screen Shot 2021-07-25 at 7 54 37 PM" src="https://user-images.githubusercontent.com/40152804/126917512-2a8f6f35-8896-489a-8dd7-3efdfbf2c788.png">

# Starting up and Activating the Blockchain

* Use the following to activate node  and start mining: ./geth --datadir *younodename* --mine --miner.threads 1
* Record the enode:// address in following output from activating node 1.
* <img width="566" alt="Screen Shot 2021-07-26 at 11 11 55 AM" src="https://user-images.githubusercontent.com/40152804/127013363-e34d0835-554a-4b66-9083-e4b3c6362272.png">
* Use the following on node 2 with the RPC flag enabled and use the enode:// address from the first node (note that port 30303 was used by node 1, so make sure to at least select port 30304 for node 2) ./geth --datadir *yournodename* --port 30304 --rpc --bootnodes "enode://<replace with node1 enode address>"
* 
  ./geth --datadir nodebeta --port 30304 --rpc --bootnodes "enode://127ecdb15b35eb8181c314d0cf6ce3ea36d3e4bf15f0001da8daf5a2c9f0adc828d805137e01df30846fde4a0a6c2947ddb7768bb5a08bd8ff7bcb3bf0729e1c@127.0.0.1:30303"

# How to Send Transactions Using MyCrypto

  
  
  
  
  
