# Token-Bouncer

Use at your own risk. Bounced tokens get burnt if you use the default address.

Welcome to the Token Bouncer! This application automatically monitors a wallet for blacklisted token IDs and bounces them (sends to another address). Checks for the blacklisted token IDs happen every 5 minutes. It will keep unwanted tokens out of your wallet!

Token Bouncer uses ThierryM1212's fantastic [Ergo Wallet CLI](https://github.com/ThierryM1212/ewc) to interact with the Ergo Blockchain.
## Setup
1. Clone the repository and enter the directory:

```
git clone https://github.com/rustinmyeye/token-bouncer
```

```
cd token-bouncer
```
   
2. Ensure Docker is installed on your system then, build the image with:
   

```
docker build -t bouncer .
``` 

3. Then to start the container:

```
docker run -p 5000:5000 -d --name token-bouncer bouncer
```
4. Navigate to the web ui at `http://localhost:5000`
5. Enter your mnemonic in the provided field below and click "Set Mnemonic".
6. Enter the Token ID's you want to bounce separated by commas (like this: tokenid, tokenid, tokenid) in the field below and click "Set Token IDs".
7. If you wish to use an address other than the default bounce address, set it in the "New Bounce Address" field.
8. The app will begin monitoring the address when the mnemonic is set.

![webui](https://github.com/rustinmyeye/token-bouncer/blob/main/Screenshot%202024-05-20%20at%2012-55-33%20Token%20Bouncer.png?raw=true)
![webuibounceall](https://github.com/rustinmyeye/token-bouncer/blob/main/Screenshot%202024-05-20%20at%2012-54-20%20Token%20Bouncer.png?raw=true)
