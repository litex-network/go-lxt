# go-lxt


### what's the litexnet

lxt-network Smart Chain starts its development based on go-ethereum fork. So you may see many toolings, binaries and also docs are based on Ethereum ones, such as the name “geth”.

But from that baseline of EVM compatible, Uuu-network Smart Chain introduces a system of 21 validators with Proof of Staked Authority (PoSA) consensus that can support short block time and lower fees. The most bonded validator candidates of staking will become validators and produce blocks. The double-sign detection and other slashing logic guarantee security, stability, and chain finality.

### Building the source

Many of the below are the same as or similar to go-ethereum.

For prerequisites and detailed build instructions please read the [Installation Instructions](https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum) on the wiki.

Building `geth` requires both a Go (version 1.14 or later) and a C compiler. You can install
them using your favourite package manager. Once the dependencies are installed, run

```shell
make geth
```

or, to build the full suite of utilities:

```shell
make all
```

### How to run Full node
    // litexnet network chainId: 19449
Steps:

1. Download the binary, config and genesis files from release, or compile the binary by make geth.
2. Init genesis state: ./geth --datadir node init genesis.json.
3. Start your fullnode: ./geth --datadir ./node --gcmode archive --networkid 19449 --bootnodes 'enode://9c5f564607acae70c27655f366ce06647b3894cf46ad785821bf29e52af485fe9ea3e910045cfb1a247a68729d22ffa0704698e271a17691b0ac4b5c35df9ba4@ 35.73.117.140:30303'
