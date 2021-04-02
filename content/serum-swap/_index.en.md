---
date: 2020-10-27T00:0:00+00:00
title: Serum Swap
weight: 1
---

[Serum Swap](https://swap.projectserum.com/#/) is a new AMM on Serum! You can find the source code on [Github](https://github.com/project-serum/oyster-swap).

{{% notice tip %}}
Try it now at: [https://swap.projectserum.com](https://swap.projectserum.com) or [https://swap.bonfida.com](https://swap.bonfida.com)
{{% /notice %}}

## How does Serum Swap work?

Like typical AMMs, you can join the pools and trade against them. The curve is the standard **x\*y=k curve**.

Solana based AMMs are fast! Serum Swap takes about **1 second to settle** a trade or pool addition/removal, and gas fees are tiny: roughly **\$0.00002** per trade.

![serum-swap](/images/articles/serum-swap/swap-form.png?classes=shadow&width=30pc)

## Is there yield?

Yes! Anyone can add yield to any pools.

But in addition: there will be **1,000,000 SRM tokens dropped** as yield over the next month!

**In particular:**

- Start time: 2020-10-28 1am HKT
- End time: 2020-11-25 1am HKT
- Total airdrop: 1m SRM
- Time: 20 random times, 50k SRM each time
- Location: 5k SRM each to the following pools:

  - SRM/BTC
  - SRM/ETH
  - SRM/USDT
  - SRM/USDC
  - SRM/SOL
  - SRM/YFI
  - SRM/LINK
  - SRM/SUSHI
  - SRM/FTT
  - SRM/FRONT

{{% notice tip %}}
Method: SRM will be added directly to the contents of the AMM pool, effectively split between all LP token holders
{{% /notice %}}

{{% notice tip %}}
Note: this is merely indicative and should there be any difficulties best efforts will be made to do what is reasonably in line with the intention.
{{% /notice %}}

## What are the fees?

Takers are charged 0.30%. Of that:

- 0.25% goes to the liquidity providers (LPs).

- 0.04% goes to a SRM buy/burn.

- 0.01% goes to the GUI hoster; you can set this in the GUI source code.

{{% notice tip %}}
The 25bp fees are tokens left in the pool
{{% /notice %}}

{{% notice tip %}}
The 4bp and 1bp fees are transfers of LP tokens
{{% /notice %}}

## How do you host a Serum Swap GUI?

### Serum Swap GUI

You will find the official repository of Serum Swap UI here: [https://github.com/project-serum/oyster-swap](https://github.com/project-serum/oyster-swap). This provides you with everything you need to start your own Serum Swap GUI.

Once you have forked the repository, you can run a local environment by running:

```bash
yarn start
```

### Collecting fees

Serum Swap allows you to collect fees for the orders made on your GUI. In order to collect the fees, you need to modify the `.env` file that looks like this:

```bash
# HOST Public Key used for additional swap fees
SWAP_HOST_FEE_ADDRESS=''

# Rewired variables to comply with CRA restrictions
REACT_APP_SWAP_HOST_FEE_ADDRESS=$SWAP_HOST_FEE_ADDRESS
```

To collect fees enter your address in the `.env` file.

### Setting your own domain name

The `package.json` file contains a field called `homepage`, change it to your name domain.

### Hosting

There are different solutions to host your GUI. You can host it for free on Github Pages or host it on your own server.

#### Github Pages

This is the easiest way of hosting and deploying a GUI, you simply have to use the following command to deploy your GUI

```bash
yarn deploy
```

The GUI will then be hosted on the `gh-pages` branch of your Github repository.

#### Hosting on your own server

Alternatively, you can host your GUI on your own server and use Nginx for instance to serve it. To create the production build run

```bash
yarn build
```

The build will be created in the `build` folder of the working directory.

## How safe is this?

While it has been tested, it has not been audited. Use at your own risk.

Furthermore, the GUI you use might not always give clear reasons for error messages. When in doubt, check your max slippage.

{{% notice warning %}}
Serum Swap has not been audited. Use at your own risk.
{{% /notice %}}

{{% notice tip %}}
Serum Swap has a 2mm SRM insurance fund
{{% /notice %}}

## Can I change the GUI?

Of course! That’s the whole point of DeFi: use this as a building block, compose with it, alter it, host it.

See what [Bonfida](http://bonfida.com/dex) and [CCAI](http://dex.cryptocurrencies.ai) have done with Serum DEXes!

{{% notice tip %}}
The Serum Swap UI uses [React](https://reactjs.org) and [Ant Design](https://ant.design) UI library. To learn how to customize it, refer to their [official guide](https://ant.design/docs/react/customize-theme)
{{% /notice %}}

## Is the AMM on-chain?

Yes! This AMM if fully **on-chain and noncustodial**.

Right now you can connect to it using Solana wallets such as [Sollet.io](https://sollet.io) or [SolFlare](https://solflare.com).

## Is this the only Serum AMM?

No! Already there’s an [off-chain AMM](https://gitlab.com/OpinionatedGeek/samm), but more -- including [Pools](https://docs.google.com/document/d/1lmMZRKkxMFOtGOEZOFEKYL7syqv-4QT87F0o55fc35Y/edit) -- are coming soon.
