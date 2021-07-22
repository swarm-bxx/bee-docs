# Kovan Testnet Example of docker-compose

It would be quite easy to setup the bee nodes of Swarm BXX on kovan testnet, which the
example prepare most of configuration here. The bee node will be launched successfully
after you complete the following steps.

## Step 1: preparing the RPC swap endpoint

You can setup your own rpc endpoint on Kovan testnet or just using the infura.io.

It is strongly recommended using [infura.io](https://infura.io/), which saves a lot of
time.

Or you may want to maintain your own rpc endpoint and the tutorial of
[kovan-testnet/rpc-node-setup](https://github.com/kovan-testnet/rpc-node-setup) may help you.

Once finished, just uncomment and replace the value of `BEE_SWAP_ENDPOINT` in `.env`
file.

## Step 2: NAT Address

To optimize the connivitity of Swarm BXX network, the NAT address must be configured
properly. You should follow the procedure of [Swarm Connectivity](https://docs.ethswarm.org/docs/installation/connectivity)

## Step 3: Launching

Just run the following command to launch the bee node:

```bash
cd dir_of_your_docker_compose
docker-compose up -d
```