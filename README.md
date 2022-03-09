# Lobeke Beacon - A Sharded Blockchain Protocol
[![Compatible with Substrate v3.0.0](https://img.shields.io/badge/Substrate-v3.0.0-GREEN)](https://github.com/paritytech/substrate/releases/tag/v3.0.0)
# Under Development
Lobeke is a the beacon chain for the mony network. It is built using the substrate framework and uses NPOS consensus algorithm. It is still under construction and more details will be shared in the final mony network whitepaper and subsquent literature.

### The network is still Under Development

## Table of Contents
- [What Lobeke DOES](#What-LOBEKE-DOES): List of system functionality

- [TODO](#TODO): List of system features

- [Installation](#Installation): Setting up Rust & Substrate dependencies

- [UI Demo](#UI-Demo): Demoing this PIM implementation in polkadot.js

- [Directions for developers](#Directions): Documentation and references if you get stuck during and after set up

- [Open Source Credits](#Helpful-Resources): Documentation and references if you get stuck during and after set up

## What LOBEKE DOES
Lobeke supports the following features:

- [ ] One-way Payment Channels
- [ ] Stable Staking Rewards
- [ ] Onchain democracy
- [ ] Onchain Identity Management
- [ ] Onchain Bounties
- [ ] Onchain treasury
- [ ] Upgrade from POA to leaderless POS
- [ ] Onchain Democracy
- [ ] Cross chain messaging


## Installation (Demoing DEV net)

### 1. Automated getsubstrate.io Script
```
#This script installs all substrate and all requirements
curl https://getsubstrate.io -sSf | bash -s -- --fast

# Manual Installation of rust
# for windows users install from https://rustup.rs instead

curl https://sh.rustup.rs -sSf | sh

# Configure

source ~/.cargo/env

rustup default stable
rustup update
rustup update nightly
rustup target add wasm32-unknown-unknown --toolchain nightly

```

## UI Demo

In this UI demo, you will interact with the Mony blockchain via the [Polkadot JS](https://substrate.dev/docs/en/development/front-end/polkadot-js).

The following demo takes you through a scenario where:
- Alice already owns LOB(native token) of value 1000000000 upon genesis
- Alice sends Bob a LOB(native token) with value 50000, tipping the remainder to validators

1. Compile and build a release in dev mode
```

# Build Wasm and native code:
cargo build --release
```

2. Start your node & start producing blocks:
```
./target/release/mony-node --dev --unsafe-ws-external

```

3. In the console, notice the helper printouts. In particular, notice the default account `Alice` was already has `10000000000 LOB` upon the genesis block.

4. Open [Polkadot JS](https://polkadot.js.org/apps/#/explorer?rpc=ws://localhost:9944), make sure the client is connected to your local node if its not then start by going to Settings > General, and selecting `Local Node` in the `remote node` dropdown.



### Directions for contributors
1. Checkout the `dev` branch. 
2. Create your branch
3. Create pull request include reason why you think your change is necessary

## NOTE
The network is still under development and so is this node. You can run it and test it out but it is not yet production ready. It will later on be merged into the mony network repo and this repository will be archived.


## Open Source Credits
In order to rapidly scale, the mony network has utilized tools and resources developed the teams at;
- [Substrate](https://substrate.io)
- [OMRL](https://github.com/open-web3-stack/open-runtime-module-library)
- [Polkadot](https://github.com/paritytech/polkadot)