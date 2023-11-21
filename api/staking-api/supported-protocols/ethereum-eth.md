# Ethereum (ETH)

The way of this page applies only to multiple 32 ETH staking.

## Environment

<table><thead><tr><th width="122">Network</th><th width="458">BatchDeposit Contract Address</th></tr></thead><tbody><tr><td>Goerli</td><td>0x80dbE42a7Da7E746689DBB737D454aCE95dFA9f7</td></tr><tr><td>Mainnet</td><td>0xf65e567fc03621E93316120A4ce596f9F5bafBEC</td></tr></tbody></table>

## API Docs

{% file src="../../../.gitbook/assets/Staking OpenAPI.pdf" %}

## Deposit User Progress

**HashQuark Operations**

1. System Operator generate pubkeys for the user
2. System Admin create broker and add API Authentication Address to the broker

**Broker Operations**

1. Give us API Authentication Address
2. Invoke `Create User` API in OpenAPI to create a user
3. Invoke `Get Deposit Data` API in OpenAPI to get deposit data for the user
4. Give user the deposit data and invoke Deposit function in Batch Deposit With ELRVault contract or invoke `Sending Transaction` API in OpenAPI to sign the unsigned transaction created in c then send
5. Invoke get deposit details / list API to check deposit details
6. After the validators are active, invoke rewards API to get user reward
7. Provide us the profit address, we will send the gas fee commission every settlement interval

## Staking With Us

Contact us to become a broker of us.
