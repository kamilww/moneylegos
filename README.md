
# moneylegos
Go Ethereum testnet with Proof of Authority consensus

# Dependencies
Go Ethereum
https://geth.ethereum.org/downloads/

My Crypto
https://www.mycrypto.com/

# Network Setup
These are the following steps to configure this testnet up from scratch:

## Step 1: Set up Accounts for Two Nodes
* Input the following command: ./geth account new --datadir *yournodename*
* Enter and confirm a password that will be used to unlock the keystore file that the program will generate
* <img width="578" alt="Screen Shot 2021-07-26 at 5 37 22 PM" src="https://user-images.githubusercontent.com/40152804/127062593-0542ae77-c3bc-463a-bf63-a814cb054e5e.png">
* Repeat this step as desired for the number nodes needed with different node names.

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
* Use the following command on for both of your nodes: ./geth init yournetworkname.json --datadir *yournodename*
* This is what the output should look like:
* <img width="568" alt="Screen Shot 2021-07-25 at 7 54 37 PM" src="https://user-images.githubusercontent.com/40152804/126917512-2a8f6f35-8896-489a-8dd7-3efdfbf2c788.png">

# Starting up and Activating the Blockchain

* Use the following to activate your first node and start mining: ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock
* Record the enode:// address in following output from activating node 1.
* Activate your second node (to also mine) with a unique port from node 1: ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
* <img width="566" alt="Screen Shot 2021-07-26 at 11 11 55 AM" src="https://user-images.githubusercontent.com/40152804/127013363-e34d0835-554a-4b66-9083-e4b3c6362272.png">

# How to Send Transactions Using MyCrypto

## Step 1
* First, you must set up a custom node on MyCrypto in order to connect to this PoA network. First select change network, and then on "Add Custom Node"
<img width="1216" alt="Screen Shot 2021-07-26 at 7 00 50 PM" src="https://user-images.githubusercontent.com/40152804/127069911-2d279c1e-df6a-45d6-808b-8dd241426b6c.png">
* You will see a screen like the following below. Make sure to use http://127.0.0.1:8545 as the URL, ETH as the currency, and the Chain ID of the network.
* <img width="582" alt="Screen Shot 2021-07-26 at 7 21 56 PM" src="https://user-images.githubusercontent.com/40152804/127071440-408558c5-8b6c-4ce7-a617-55a4890c9a3e.png">
* 
* Click change network, and select the custom network you created.

## Step 2
* Click on either "Private Key" or "Keystore File" and follow the prompts to unlock your node accounts.
* You will see the following screen. Follow the prompts to send a transaction
<img width="1215" alt="Screen Shot 2021-07-26 at 7 39 36 PM" src="https://user-images.githubusercontent.com/40152804/127072696-3447afc2-880f-4e29-9e82-6a0dcb977acd.png">
<img width="1222" alt="Screen Shot 2021-07-26 at 7 40 22 PM" src="https://user-images.githubusercontent.com/40152804/127072763-4e0bfa11-e829-4911-9bae-364ffdf5ded7.png">
<img width="1353" alt="Screen Shot 2021-07-26 at 8 10 04 PM" src="https://user-images.githubusercontent.com/40152804/127074842-473cc130-ab39-4f1a-a624-9ed281c73bdf.png">

  
  
