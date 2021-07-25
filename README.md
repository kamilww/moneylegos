# moneylegos
Go Ethereum testnet with Proof of Authority consensus

# Dependencies
Go Ethereum
https://geth.ethereum.org/downloads/

# Network Setup
These are the following steps to set this testnet up from scratch and explore using Geth and MyCrypto:

## Step 1: Set up two different public/private keypairs in MyCrypto
* Open up MyCrypto, and select "Create New Wallet"
<img width="1221" alt="Screen Shot 2021-07-25 at 5 13 08 PM" src="https://user-images.githubusercontent.com/40152804/126913669-886df5d3-7c64-48fc-aed4-fea18350e0cf.png">

* Select Generate a Wallet under "Create New Wallet"
<img width="1241" alt="Screen Shot 2021-07-25 at 5 15 04 PM" src="https://user-images.githubusercontent.com/40152804/126913714-7299b19a-fb07-4e15-b86c-85c0503ace67.png">

* Select Generate a Keystore File under "Keystore File"
<img width="1239" alt="Screen Shot 2021-07-25 at 5 22 31 PM" src="https://user-images.githubusercontent.com/40152804/126913879-6aa710f8-f2e0-443f-91aa-c9562d065ec1.png">

* Enter and confirm a password for unlocking your Keystore File
<img width="1247" alt="Screen Shot 2021-07-25 at 5 29 10 PM" src="https://user-images.githubusercontent.com/40152804/126914041-4fa60c0e-7e8a-4425-ac3e-e0d9ef0882a9.png">

* Click Download Keystore file and install in directory of your choice.
* Then, after downloading your keystore file, store the given private key.
* Repeat the above steps for the second keypair

## Step 2
* Log into each account created under step 3 in MyCrypto either using the stored private key or the generated keystore file.
* Obtain and record the public and private key for the keypairs generated under step 3.
<img width="1245" alt="Screen Shot 2021-07-25 at 5 42 57 PM" src="https://user-images.githubusercontent.com/40152804/126914374-d34b89de-334f-4353-b8a4-67e0501fdfd2.png">

## Step 3: Initialize the network using CLI
* You could use any network name you like as long as it follows the naming convention specified by geth.
<img width="583" alt="Screen Shot 2021-07-25 at 3 33 09 PM" src="https://user-images.githubusercontent.com/40152804/126911113-d4b2a16b-0c09-4fda-a5f0-9aad9437561b.png">

## Step 4: Network Configuration
* Select option 2 (Configure new genesis) for "What would you like to do?"
* Then select option 1 (Ceate new genesis from scratch) for another "What would you like to do?" prompt.
* Next, select option 2 (Clique - proof-of-authority) for consensus engine.
* This testnet was left with the default blocktime of 15 seconds.
* <img width="372" alt="Screen Shot 2021-07-25 at 4 57 11 PM" src="https://user-images.githubusercontent.com/40152804/126913272-63fcd56c-71b6-4529-af99-7dedbc2f7dc1.png">

## Step 5: More Network Configuration
* Select which of the accounts from step 1 are allowed to seal (once finished with selection, press enter on next "0x" prompt)
* Select which accounts from step 1 should be prefunded
* Precompiled-addresses do not need to be prefunded, so no was selected
* Specify your chain/network ID or choose random by not providing an ID (this information can be looked up later)

<img width="570" alt="Screen Shot 2021-07-25 at 6 02 09 PM" src="https://user-images.githubusercontent.com/40152804/126914800-e91b5e19-bf62-466f-9eab-a93a1f473016.png">

## Step 6: Exporting Network Configurations
* Select option 2: "Manage existing genesis"
* Next, select option 2: "Export genesis configurations"
* Choose which folder you would like to save the genesis configuratio in.
*<img width="567" alt="Screen Shot 2021-07-25 at 6 05 38 PM" src="https://user-images.githubusercontent.com/40152804/126914873-d7535323-5039-495c-9b57-757ebdc8e681.png">

## Step 7: Creating Nodes
* crtl+c puppeth
* Input the following command with corresponding flag: ./geth account new --datadir <yournodename>
* Enter and confirm a password to unlock this.
  <img width="568" alt="Screen Shot 2021-07-25 at 7 27 27 PM" src="https://user-images.githubusercontent.com/40152804/126916779-eccfdfb5-c29c-4da2-9ccc-      fcce730cb39a.png">
* Repeat this step with at least one other node using a different nodename.
## Step

  
# How to Activate Network

# How to Send Transactions Using MyCrypto
