# router-pingpong

## install dependencies
```shell
pnpm install 
```

## PingPong Test

### Deploy Contracts to both networks
First adjust the gateway address in `scripts/deploy.ts` to the one found in https://docs.routerprotocol.com/networks/supported-chains#for-testnet

After deploy the PingPong contract on the different networks

```shell
npx hardhat run scripts/deploy.ts --network <network>
```
e.g. to arbitrum-sepolia and sapphire-testnet

### Register Feepayer for contract in RouterProtocol
Connect with your account which you specified as feepayer while deploying on this website
(In the deploy.ts it is the deployer address by default)
https://testnet.routerscan.io/feePayer

To be deployed contracts should appear here and need to be approved.

hint: if the contracts aren't showing up here, you deployed the contract with the wrong gateway address

### Run PingPong test

```shell
npx hardhat run scripts/pingpong.ts --network <network>
```

