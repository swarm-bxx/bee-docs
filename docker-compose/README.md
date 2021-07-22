# Kovan Testnet Example of Docker Compose

It would be quite easy to setup the bee nodes of Swarm BXX on kovan testnet, which the example prepare most of configuration here. The bee node will be launched successfully after you complete the following steps.

## Step 1: Preparing the RPC swap endpoint

You can setup your own rpc endpoint on Kovan testnet or just using the infura.io.

It is strongly recommended using [infura.io](https://infura.io/), which saves a lot of time.

Or you may want to maintain your own rpc endpoint and the tutorial of [kovan-testnet/rpc-node-setup](https://github.com/kovan-testnet/rpc-node-setup) may help you.

Once finished, just uncomment and replace the value of `BEE_SWAP_ENDPOINT` in `.env` file.

## Step 2: (Optional) NAT Address

To optimize the connivitity of Swarm BXX network, the NAT address must be configured properly. You should follow the procedure of [Swarm Connectivity](https://docs.ethswarm.org/docs/installation/connectivity)


## Step 3: Set BEE_PASSWORD

Change the `BEE_PASSWORD` value in `.env` file as your own custom password.

## Step 4: Launching bee node on Docker

Just run the following command to launch the bee node:

```bash
cd dir_of_your_docker_compose
docker-compose up -d
```

## Step 5: Faucet

It is required that one bee node must have sufficient fund to connect to the Swarm BXX testnet network:

- Kovan ETH
- BXX 

### Kovan ETH Faucet

Kovan ETH can be sprinkled here: https://linkfaucet.protofire.io/kovan

### BXX Faucet

1. Join [BXX Discord](https://discord.gg/65c5wBtaeB) channel
2. Go to channel of `Faucet` and type slash command to get BXX faucet:

    ```
    /faucet <your ethereum address>

    # Example:
    /faucet 0x80F9fF4A2f0b6D55076aFC91AB8746A84bDA0bDf
    ```

    After minutes you will get 50 BXX to launch your node.
