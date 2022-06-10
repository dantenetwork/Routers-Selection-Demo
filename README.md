# Routers Selection Demo

This is a demo for a simulation of routers Selection Algorithm(on-chain) deployed on NEAR.

Attention: the testnet and mainnet of NEAR cannot be accessed in some areas.
For convenience, we are building a version that can be accessed from discord. It's coming soon.

## Prepare

### NEAR cli

* Installation: [Tutorials](https://docs.near.org/docs/tools/near-cli#installation)

### Account on NEAR testnet

* Create account on testnet: [wallet testnet](https://wallet.testnet.near.org/)

* Use the account in near cli:

```sh
near login 
```

### Contract on NEAR testnet

Contract id:

`Testnet`: 4b588bc0cd98a440eaf55307552e1a2b3ae3818e0978e5e359cb8406d7c38827

## Usage

```sh
export SELECTOR="4b588bc0cd98a440eaf55307552e1a2b3ae3818e0978e5e359cb8406d7c38827"
```

### Query all validators

The following command simulates show all validators.

```sh
near view $SELECTOR get_validators
```

## Select validators randomly

The following command simulates randomly select `nums` validators from all validators.

```sh
near call $SELECTOR select_validators '{"nums": 1 }' --accountId $SELECTOR --gas 300000000000000
```

### Query selected validators

The following command simulates show all selected validators.

```sh
near view $SELECTOR get_selected_validators
```
