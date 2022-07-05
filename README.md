# Indexing an Avalanche Local Subnet with The Graph

## Introduction

Avalanche is an open-source platform for launching decentralized applications and enterprise blockchain deployments in one interoperable, highly scalable ecosystem. Avalanche is the first decentralized smart contracts platform built for the scale of global finance, with near-instant transaction finality. Avalanche is a blockchain that promises to combine scaling capabilities and quick confirmation times through its Avalanche Consensus Protocol. It can process 4,500 TPS (transactions per second). For Ethereum, that number is 14 TPS.

![avax](/images/1.jpeg "avax")

Blockchains have traditionally been referred to as being slow and unscalable. Avalanche embraces an innovative approach to concensus that solve these problems without compromising on security.

Avalanche is a high-performance, scalable, customizable, and secure blockchain platform. It targets three 15 broad use cases:

* Building application-specific blockchains, spanning permissioned (private) and permissionless (public)
deployments.
* Building and launching highly scalable and decentralized applications (Dapps).
* Building arbitrarily complex digital assets with custom rules, covenants, and riders (smart assets).

# Avalanche features 3 built-in blockchains: 
* Exchange Chain (X-Chain)
* Platform Chain (P-Chain)
* Contract Chain (C-Chain)

The P-chain is for platform management. It handles requests related to the validator, the subnet, and the blockchain. 
The C-chain is for contract management. It is based on EVM; hence its API is almost identical to other EVM protocols. It has both RPC and WebSocket endpoints, and it handles requests for smart contracts. 
The X-chain is for asset exchange. It is Avalanche’s native platform; it is used for creating and trading assets like AVAX and NFTs. 

These 3 blockchains are secured by the Avalanche Primary Network with is a special kind of subnet.

The Avalanche Architecture is composed of:
* Subnetworks
* Virtual Machines

# The Graph Protocol

The Graph is an open-sourced indexing protocol for organising blockchain data and making it easily accessible using GraphQL. This software collects, processes and stores data from various blockchain applications to facilitate effecient information retrieval. The Graph stored data into various indices called Subgraphs, allowing applications to query it. These queries are initiated using GraphQL, a language originally created by facebook. The Graph has the ability to query networks like Ethereum and IPFS. Anyone can build and publish open subgraphs.


![graph](/images/21.png "graph")

## Prerequisites

### NodeJS and Yarn

First, install the LTS (long-term support) version of [nodejs](https://nodejs.org/en). This is `16.2.0` at the time of writing. NodeJS bundles `npm`.

Next, install the [yarn](https://yarnpkg.com) package manager:

```zsh
npm install -g yarn
```

### Git

To check the current Git version use:

```zsh
git --version
```


# Roadmap

This tutorial is created to serve as a guide to help developers setup an Avalanche Subnet and Index them using graphQl. We are going to learn how to run a local network using the `avalanche-cli` and deploy a basic smart contract using `Remix` and `Hardhat`. Then Lastly we will be indexing our subnet using The Graph. This guide is an extension of the [Official Avalanche Documentation]().

Please note that all command line inputs and sample codes are MacOs and Linux Based. Commands may vary for other operating systems.

In summary, we will be discussing the following:
1. Running an EVM Subnet on the Local Network using the Avalanche-cli
2. Setting up metamask
3. Deploying smart contracts with Remix
4. Working with Hardhat