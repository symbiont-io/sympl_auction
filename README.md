# Auction smart contract

<a href="https://portal.symbiont.io/sdk_docs/docs/intro"><img src="https://img.shields.io/badge/Assembly-4.5.0-orange"/></a>
<a href="https://portal.symbiont.io/sdk_docs/docs/intro"><img src="https://img.shields.io/badge/Assembly%20SDK-2.0.3-blue"/></a>

## Introduction

This smart contract repository is a sample `symPL` contract as is used in the [Auction walkthrough](https://iportal.symbiont.io/sdk_docs/docs/walkthroughs/auctions/auctions/index/index.html) 
of Symbiont's SDK documentation. Hereby included are:
- the smart contract `auction.sympl`
- the contract definition `contract.yaml`
- A pytest test to validate the smart contract `test/auctions_test.py`

## Model

### Roles
- Creator (Key Alias)
- Key Alias

### Channel topology
- Public channel

### Actions

| Action         | Channel | Role |
|----------------|---------|------|
| Create Auction | Public  | Any  |
| Make Bid       | Public  | Any  |
| Close Auction  | Public  | Creator |
| Pass Day       | Public  | Any  |

## Contributing 

Anyone is welcome to contribute to this repository, be it in the form of features, bug fixes, documentation or additional
tests. 
Please create a branch of your own and submit for merge via merge request. A codeowner will be assigned your merge request
and provide feedback/merge it. 

## Running tests

Requirements:
- Install the [pytest plugin](https://iportal.symbiont.io/sdk_docs/docs/testing/index/index.html)
- Have a mock-network running (we recommend using `sym` to get a mock network up and running quickly)

Steps: 
- Change directory to the root of this repository
- Run the following command:
```shell
pytest test/auctions_test.py --network-config=~/.symbiont/assembly-dev/mock-network/default/network-config.json --contract-path=./
```

