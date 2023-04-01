# Anon-Fed-AI Smart Contract Service

This service manages the Ethereum smart contract for the Anon-Fed-AI system. The smart contract is responsible for aggregating model updates, verifying zk-SNARK proofs, and sharing the global model. The service stores the global model on IPFS and maintains the IPFS hash in the smart contract.

## API

This service provides a REST API with the following endpoints:

- `POST /train`: Initiates training for a client by submitting a hashed model update to the smart contract.

- `POST /verify`: Verifies a zk-SNARK proof submitted by a client for the corresponding model update.

- `GET /model`: Retrieves the current global model from IPFS and returns it as a byte stream.

## Installation

To run this service, you must have the following installed:

- Node.js
- Truffle
- Ganache CLI

Once you have these installed, you can run the service using the following command:

truffle migrate --reset
npm start


## Configuration

This service requires the following environment variables to be set:

- `MNEMONIC`: The mnemonic for the Ethereum account to use for deploying the smart contract.
- `INFURA_API_KEY`: The API key for the Infura node to use for deploying the smart contract.

## Contributing

Contributions to this service are welcome. To contribute, please fork this repository, create a new branch with your changes, and submit a pull request.
