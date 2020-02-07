Masternode SETUP guide
Before you start, you must have required amount of coins (5000 MOCHA), a desktop wallet installed and fully synchronized and VPS with minimum 1gb of RAM and and one of the following OS:

Ubuntu 16.04 / 17.10 / 18.04 / 19.04
Debian 8 / 9 / 10
CentOS 6 / 7 / 8
Fedora 27 / 28 / 29 / 30 / 31

DESKTOP WALLET SETUP
The first thing you should do is set up your desktop wallet. Here are the steps for Windows/Linux or macOS Wallet

1. Open the MochaChain Core Desktop Wallet.
2. Go to RECEIVE and create a New Address: MN1
3. Send 5000 MOCHA to MN1.
4. Wait for 15 confirmations.
5. Go to Tools -> Debug console  Console
6. Type the following command: masternode outputs 7. In addition type this: masternode genkey
8. Go to Tools -> Open Masternode Configuration File
9. Add the following entry:


Alias Address Privkey TxHash Output_index
Your entry should look something similar to this:

MN1 100.110.120.130:21103 8cgavwCh2f6uriUXtiY8x4Vsgz95BipPmuhiw5K5TtA9gjSAH5Q 13d196c1fd676c0bf074dd54f79f8904e59d31f23ed2a852a19382dee95a3aa9 1
Alias: MN1
Address: VPS_IP:21103
Privkey: Masternode Private Key from step 7
TxHash: First value (HEX STRING) from Step 6
Output index: Second value (INTEGER) from Step 6
10. Save and close the file. Restart Wallet.
11. Setup VPS (see below)
12. Go to Masternode Tab. If you tab is not shown, please enable it from: Settings  Options  Wallet  Show Masternodes Tab
13. Click Update status to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is unlocked.
14. Open Debug Console and type:

startmasternode alias false MN1

VPS Setup
wget https://mocha.network/mochamnautosetup.sh 
sudo bash mochamnautosetup.sh
During installation, enter the key from STEP 7 when prompted
