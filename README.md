# Linear timelock token User Interface (UI)

# What does it do?

Interacts with the type of timelock smart contract, which allows users to unlock tokens.


# How do end users interact with the timelock UI

Users simply load the page, (the user's account details are automatically pre-filled in the address input box). 

The user's available (un-lockable) balance is calculated automatically. 

The user then simply clicks the "Unlock Your Tokens" button (please note: the maximum amount of available tokens are automatically pre-filled in the amount input box). 

It is recommended to also click the "Refresh/Calculate Balances" button after any transfers.

![Screen Shot 2022-01-10 at 7 20 09 am](https://user-images.githubusercontent.com/9831342/148701427-3217e79a-3e02-4b71-b4b1-20d93729ac94.png)

# Where is the timelock smart contract

There are a few different [timelock smart contracts i.e.](https://github.com/second-state/linear-timelock-smart-contract/) which are deployed on the Ethereum mainnet. 

# How to deploy this UI

Clone this repository

```
git clone git@github.com:second-state/linear-timelock-user-interface.git
```

## ABI and address of Timelock

Paste the ABI **and the address** of the linear timelock's successfully deployed contract instance, into the helper.js file

## Contract address of ERC20 (NOT timelock)

In addition to that, also paste the contract address of the **ERC20 contract** into the helper.js file. You will see the two addresses are clearly marked.

## Installing

Then simply type

```
npm install
```

## Running

To publish/deploy simply type

```
npm run deploy
```

## Convention for URL

The path prefix is 

```
claim-parastate-erc20-token
```

The 3 parameters are `locking`, `cliff` and `vesting`. For example.

```
_locking-na_cliff-na_vesting-na`
```

When combined will produce URL paths like the following examples

no locking, no cliff and no vesting

```
claim-parastate-erc20-token_locking-na_cliff-na_vesting-na
```

30 Day lock, no cliff and no vesting

```
claim-parastate-erc20-token_locking-30-day_cliff-na_vesting-na
```

no locking, 90 day cliff and 15 months vesting

```
claim-parastate-erc20-token_locking-na_cliff-90-day_vesting-15-month
```


This particular site will be hosted to [https://second-state.github.io/claim-parastate-erc20-token_locking-30_cliff-na_vesting-na/html/index.html](https://second-state.github.io/claim-parastate-erc20-token_locking-30_cliff-na_vesting-na/html/index.html)
