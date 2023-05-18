# Crowdfunding Project

This project implements a crowdfunding application using smart contracts on the Ethereum blockchain.

## Contracts

### CrowdFundingV1.sol

This contract represents the version 1 of the crowdfunding contract. It allows users to create campaigns, donate to campaigns, and retrieve information about campaigns. Each campaign has an owner, title, description, category, funding target, deadline, amount collected, image, list of donators, and corresponding donation amounts.

### CrowdFundingV2.sol

This contract represents an upgraded version (V2) of the crowdfunding contract. It introduces additional functionality and improvements over V1. The main enhancement in V2 is the requirement that campaign deadlines must be set in the future during campaign creation.

### BoxV1.sol

This contract represents a simple example contract that stores a single value. It provides a function to retrieve the stored value.

### BoxV2.sol

This contract is an upgraded version (V2) of the Box contract. It introduces the ability to set the stored value in addition to retrieving it.

### ProxyAdmin.sol

This contract is responsible for managing upgradeable proxies. It provides functions to change the admin and upgrade the implementation of a proxy. It is used to control the upgrade process of the crowdfunding contracts.

### UpgradeableProxy.sol

This contract is an upgradeable proxy implementation that allows for transparent upgrades of contract implementations. It is used as a proxy for the crowdfunding contracts, enabling seamless contract upgrades without disrupting the existing deployed instances.

## Scripts

### donate_on_proposal.py

This script allows users to donate to a campaign by interacting with the CrowdFunding contract. It prompts the user for the campaign ID and donation amount, and then initiates the donation transaction on the Ethereum network.

### helpful_scripts.py

This script contains various helper functions used by other scripts. It includes functions for retrieving the user's account, encoding function data, and performing contract upgrades.

### upgrade_funding.py

This script demonstrates how to upgrade the CrowdFunding contract from V1 to V2 using an upgradeable proxy. It deploys the V2 contract, retrieves the proxy and admin instances, and performs the upgrade process.

## Getting Started

1. Install dependencies: `pip install -r requirements.txt`
2. Configure your blockchain network in `brownie-config.yaml` to connect to an Ethereum network or local development environment.
3. Deploy the contracts using Brownie: `brownie run deploy_contracts`. This will deploy the V1 version of the CrowdFunding contract and the BoxV1 contract.
4. Interact with the contracts using the provided scripts. You can run `brownie run donate_on_proposal` to donate to a campaign or `brownie run upgrade_funding` to upgrade the CrowdFunding contract to V2.

## License

This project is licensed under the [MIT License](LICENSE).
