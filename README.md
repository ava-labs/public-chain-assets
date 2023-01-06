# public-chain-assets

This repo holds information about subnet chains that exist on the Avalanche
network.

## To add your subnet to this list, please make a pull request that adds the following: 

Each chain in the `chains` folder may contain the following files:
- `genesis.json`: To get started, use the
  [Avalanche CLI](https://github.com/ava-labs/avalanche-cli) to enter your desired configuration parameters and copy over the resulting file using the `export` command.
- `chain-information-rpc.json`: Minimum information about the chain for a node to be able to connect to your network.


### Additional Explorer Information
- `chain-information.json`: Complete information about a network to connect to the [Avalanche Explorer](https://subnets.avax.network/).
- `token-list.json`: A list of token contracts that exist on the chain with
  information about each. These tokens have been verified using the contract
  verifier at https://subnets.avax.network/tools/verify-contract.


### Optional Information
- `upgrade.json`: Contains network upgrades for the chain, *required* for all nodes if implemented. For more information, see 
  https://docs.avax.network/subnets/subnet-upgrade#network-upgrades.
- `airdrop.json`: Contains a list of addresses that were airdropped tokens in genesis. Note: this file must be referenced in the chain config and the hash must be specified in genesis. This can also be included in the `genesis.json` file directly, see [Avalanche CLI](https://github.com/ava-labs/avalanche-cli).
