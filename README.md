# Token-Bouncer

WORK IN PROGRESS! DONT USE THIS WITH YOUR MAIN WALLET! IM AN IDIOT OK?!?!

Welcome to the Token Bouncer! This application automatically monitors a wallet for specific token IDs and bounces (sends to another address) any blacklisted tokens found. Checks for the blacklisted token IDs happen every 5 minutes.
## Setup
1. Clone the repository and enter the directory:

```
git clone https://github.com/rustinmyeye/BBC-Bouncer
```

```
cd BBC-Bouncer
```
   
2. Ensure Docker is installed on your system then, build the image with:
   

```
docker build -t bouncer .
``` 

3. Then to start the container:

```
docker run -p 5000:5000 -d --name Token-Bouncer bouncer
```
4. Navigate to the web ui at `http://localhost:5000`
5. Enter your mnemonic in the provided field below and click "Set Mnemonic".
6. Enter the Token ID's you want to bounce (separated by commas) in the field below and click "Set Token IDs".
7. If you wish to use an address other than the default bounce address, set it in the "New Bounce Address" feild.

![webui](https://github.com/rustinmyeye/BBC-Bouncer/blob/main/Screenshot%202024-05-12%20at%2020-45-01%20Token%20Bouncer.png?raw=true)
