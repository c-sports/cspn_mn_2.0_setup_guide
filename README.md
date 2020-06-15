# CSPN Masternode 2.0 Setup Guide

## Preparing your wallet

1. Open the wallet Preferences.

2. Switch to the "Wallet"-Tab and enable "Coin Control Features".

## Open the CSPN Masternode Setup Tool (Setup Tool)

1. Visit https://mntool.crypto-sports.io/ (right click -> open new tab)

***

## Creating the Addresses:

**Segwit Payout Address** 

1. Open your wallet console and type "getnewaddress Payout p2sh-segwit".

2. Send 1-10 CSPN to this address.

3. Write the address down in a note for later use.

4. Put the Payout Address into the "Payout Address"-Field of the Setup Tool. 

Tip: You can always reuse the Segwit Payout Address for future Masternode Instances.

**Masternode Collateral Address** 

1. Go to the Receive-Tab and create a new Address and label it "MN1" for example.

**Masternode Owner Address** 

1. Create another Address and label it "O1" for example.

2. Put the Owner Address into the "Owner Address"-Field of the Setup Tool.

***

## Sending the Masternode Collateral

1. Send exactly **1337 CSPN** to the Masternode Collateral Address we just created (in this case "MN1").

2. Go to the "Transactions"-Tab, right click the Transaction and click on "Copy transaction ID".

3. Wait for the transaction to reach 1 Confirmation, open the wallet  console and type "masternode outputs".

4. Now paste the transaction id you just copied into the input field (helps finding the right tx if you run multiple nodes), search for it in the "masternode outputs"-list and copy the txid's index.

5. Put the txid and index into the corresponding fields of the Setup Tool.

6. Go to the "Send"-Tab and click on "Inputs..." under Coin Control Feautures.

7. Switch to "List mode", right click the collateral you just sent and select "Lock unspent" (prevents spending of the collateral when sending coins, e.g setting up multiple Masternodes).

***

## Setting up the VPS

1. Follow the steps provided in the VPS Setup Guide: https://gitlab.com/snippets/1974167 (right click -> open new tab)

2. Put the Server IP, Ports and BLS Public Key into the corresponding fields of the Setup Tool

***

## Activating the Masternode

1. After all information has been filled into the Setup Tool, hit the "Generate"-Button.

2. Click on "Copy Command", paste it into your wallet console and execute it (Make sure your Masternode Collateral Transaction has at least 10 Confirmations)

3. Your Masternode will be active when the Activation Transaction reached 1 Confirmation.

Done.

***

## Multi Masternode Setup

Repeat the steps above while creating new Addresses (MN2, O2, (Payout Address can be reused)) and simply run the Install Script from the VPS Setup Guide again.
