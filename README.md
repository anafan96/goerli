# {Görli,Kotti} Testnet
The `--goerli` and `--kotti` cross-client proof-of-authority testnet configurations. [![Chat on Gitter](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/goerli/testnet)

- https://goerli.net

There are many Ethereum testnets available for experimenting with smart contracts and deploying decentralised applications before going live on the main Ethereum network. However, there is no testnet available that is both widely usable across all client implementations, and robust enough to guarantee consistent availability and high reliability. This is what **Görli** tries to be for Ethereum and **Kotti** for Ethereum Classic. Read more on the motivation in the [Testnet Proposal](https://dev.to/5chdn/the-grli-testnet-proposal---a-call-for-participation-58pf).

### Meta data: Görli

See also: [Getting started with the Görli Testnet](https://mudit.blog/getting-started-goerli-testnet/).

- Name: **Görli**
- Machine-readable name: `goerli`
- Stage: _launched_
  - PoA Engine: `clique`
  - Epoch interval: `30000`
  - Step period: `15`
  - Genesis hash: `0xbf7e331f7f7c1dd2e05159666b3bf8bc7a8a3a9eb1d518969eab529dd9b88c1a`
  - Network ID: `5`
  - Chain ID: `5`
  - Homestead: `0`
  - Byzantium: `0`
  - Constantinople: `0`
  - Petersfork: `0`
  - Istanbul: `1_561_651`
- Status Dashboard: 
  - https://stats.goerli.net/
  - https://goerli.ethstats.io/
- Block Explorer: 
  - https://goerli.etherscan.io/
  - https://expedition.dev/?network=goerli
- Faucets:
  - https://goerli-faucet.dappnode.net/
  - https://faucet.goerli.mudit.blog/
  - https://goerli-faucet.slock.it/
- Open RPC Endpoints:
  - https://goerli.prylabs.net
  - https://rpc.goerli.mudit.blog
  - https://rpc.slock.it/goerli
  - wss://goerli.eth.6120.eu/ws (via https://6120.eu)
- Gitter: https://gitter.im/goerli/testnet/

Please see [goerli.genesis](geth/goerli.genesis) for a genesis file compatible with Hyperledger Besu (formerly Pantheon) or Geth.

Please see [goerli.json](parity/goerli.json) for a chain specification compatible with Nethermind or Parity Ethereum.

Please see [bootnodes.txt](bootnodes.txt) if you fail connecting to the network.

### Meta data: Kotti (Classic)

- Name: **Kotti** (Classic)
- Machine-readable name: `kotti`
- Stage: _launched_
  - PoA Engine: `clique`
  - Epoch interval: `30000`
  - Step period: `15`
  - Genesis hash: `0x14c2283285a88fe5fce9bf5c573ab03d6616695d717b12a127188bcacfc743c4`
  - Network ID: `6`
  - Chain ID: `6`
  - Homestead: `0`
  - Atlantis: `716_617`
  - Agharta: `1_705_549`
  - Phoenix: `2_200_013`
- Status Dashboard: 
  - https://stats.kotti.goerli.net/
  - https://kotti.etcnodes.org/
  - http://kotti.etcstats.org/
- Block Explorer:
  - https://blockscout.com/etc/kotti/
  - http://kotti.etccoopexplorer.com/
  - https://expedition.dev/?network=kotti
  - http://kotti.ethereumtest.net/
- Faucets:
  - http://kottifaucet.me/
  - http://kotti.little-dripper.com/
  - http://kotti.etherdrip.net/
- Open RPC Endpoints:
  - https://www.ethercluster.com/kotti
- Gitter: https://gitter.im/goerli/kotti/

Please see [kotti.genesis](geth/kotti.genesis) for a genesis file compatible with Multi Geth.

Please see [kotti.json](parity/kotti.json) for a chain specification compatible with Nethermind or Parity Ethereum.

Please see extract bootnodes from the Parity chain spec if you fail connecting to the network.

### Connecting the clients

All clients supporting the Clique engine (EIP-225) are able to sync with Görli or Kotti.

##### Go-Ethereum

You can connect Geth to Görli by executing `geth --goerli`. https://github.com/ethereum/go-ethereum/releases

You can connect Core-Geth to Kotti by executing `geth --kotti`. https://github.com/etclabscore/core-geth/releases


##### Open-Ethereum (formerly Parity Ethereum)

Connect to Görli using the Clique engine: `openethereum --chain goerli` https://github.com/openethereum/openethereum/releases

Connect to Kotti using the Clique engine: `openethereum --chain kotti`

##### Hyperledger Besu (formerly Pantheon)

Connect to Görli using Hyperledger Besu by executing `besu --network=goerli`. https://github.com/hyperledger/besu/releases

Connect to Kotti using Hyperledger Besu by executing `besu --network=kotti`.

##### Nethermind

Connect to Görli by using the provided goerli.cfg included in Nethermind 0.9.1: https://github.com/NethermindEth/nethermind/releases

```
dotnet run --config configs/goerli.cfg
```

##### EthereumJS

Connect to Görli by using the provided state and genesis included in EthereumJS 0.6.1: https://github.com/ethereumjs/ethereumjs-common/releases

```
./bin/cli.js --network goerli
```

### Contribute

Run a node, [report bugs](https://github.com/goerli/testnet/issues), and join our [Gitter](https://gitter.im/goerli/testnet)!

Donations for development and hosting can be done through our mini-DAO at [`0x6974df01bf293ab9af66127c03aac79b81d494c7`](https://etherscan.io/address/0x6974df01bf293ab9af66127c03aac79b81d494c7). <3

The 2-of-3 multi-signature wallet is controlled by the following parties:

- Aidan Hyman (@chainsafeth)
- Afri Schoedon (@q9f)
- María Paula Fernández (@MPtherealMVP)
