# Motile Coin
Shell script to install an Motile Coin Masternode](http://motilecoin.io/) on a Linux server running Ubuntu 16.04. Use it on your own risk.  

***
## Installation:  

wget -q https://raw.githubusercontent.com/zoldur/MotileCoin/master/motile_install.sh  
bash motile_install.sh
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Motile Coin Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **5000** MIE to **MN1**.  
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Donation address: leave blank (or use my MIE address if you would like to donate :blush: )
* Donation %: leave blank  (or donate a small percentage :blush: )
9. Click **OK** to add the masternode  
10. Click **Start All**  

***

## Multiple MN on one VPS:

Whilst not recommended, it is possible to run multiple **Motile** Master Nodes on the same VPS. Each MN will run under a different user you will choose during installation.  

***


## Usage:  

For security reasons **Motile** is installed under **motile** user, hence you need to **su - motile** before checking:    

```
MOTILE_USER=motile #replace motile with the MN username you want to check

su - $MOTILE_USER  
Motiled masternode status  
Motiled getinfo  
```  

Also, if you want to check/start/stop **Motile** , run one of the following commands as **root**:

```
MOTILE_USER=motile  #replace motile with the MN username you want to check  
  
systemctl status $MOTILE_USER #To check the service is running.  
systemctl start $MOTILE_USER #To start Motile service.  
systemctl stop $AMOTILE_USER #To stop Motile service.  
systemctl is-enabled $MOTILE_USER #To check whetether Motile service is enabled on boot or not.  
```  

***

  
Any donation is highly appreciated  

**MIE**: M8nLjcEjPu3WTNGXEoEFj6yBDemMisWhsX  
**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LXrWbfeejNQRmRvtzB6Te8yns93Tu3evGf  

