---
date: 2020-12-06T00:0:00+00:00
title: Tokens in the ecosystem
weight: 9
---

# Maps

Maps.me is one of the world’s premium navigation apps, with over 100m users worldwide.

**Status** Not listed

**Website** [https://maps.me/](https://maps.me/)

**Contact** [https://maps.me/contacts](https://maps.me/contacts)

# Oxygen

Oxygen is a DeFi prime brokerage protocol to help you generate yield, liquidity, and more.

**Status** Not listed

**Website** [https://oxygen.org/](https://oxygen.org/)

**Contact** [contact@oxygen.org](mailto:contact@oxygen.org)

# Media

The Meda Network is an open source, decentralized and censorship-resistant live streaming hosting protocol.

**Status** Not listed

**Website** [https://mediaserver.express](https://mediaserver.express)

**Contact** [https://twitter.com/mediafndn](https://twitter.com/mediafndn)

# Bonfida

Bonfida is the full product suite that bridges the gap between Serum, Solana and the user. It's the flagship Serum GUI and bring first of its kind Solana data analytics to the field. Its API is used by some of the largest market makers as well as CoinMarketCap and CoinGecko.

**Status** Not listed

**Website** [https://bonfida.com](https://bonfida.com)

**Contact** [https://twitter.com/bonfidadotcom](https://twitter.com/bonfidadotcom)

# Pools

## What are Pools?

[Pools](http://dex.projectserum.com/#/pools) are a flexible, fundamental primitive on Serum. Each pool has the following properties:

1. A set of assets (SPL tokens)
2. A set of Pool Tokens representing ownership of those assets
3. The ability to create or redeem the pool
4. (optional) admin ability to use the assets in the pool

Pools are a way for a group of users to take collective action.

## What are examples of pools?

- Pools can act as automated market makers:
  - Each pool token owner has proportional claims on the assets in the pool
  - The pool’s asset admin key can be a program that uses the assets to provide liquidity on e.g. a Serum DEX orderbook
  - Creations and redemptions allow users to enter and exit the pool
- Pools can give yield
  - Each pool token gives fractional ownership of the pool’s assets, so dropping assets into the pool essentially gives them to the pool token holders
- Pools can act as collective investment baskets
  - The pool can rebalance its assets on e.g. a Serum DEX
  - The pool can rebalance either actively or passively

## How do fees work?

There are three fees on pool creations and redemptions. When a user U initializes a new pool, they set a fee rate (F).

- F/2.5 is paid to U
- F/2.5 (min 0.01%) is paid to LQID governance
- F/5 (min 0.005%) is paid to the GUI host

If you host a Pool GUI, you can set the address you want the F/5 GUI fees paid to.

## What are admin keys?

When you initiate a pool, you can choose whether or not to use an admin key. If you do, then that address has the ability to:

- Add tokens to the list recognized by the pool
- Remove tokens to the list recognized by the pool
- Deposit or withdraw assets from the pool
- Modify the pool’s fee
- Pause and unpause pool creations/redemptions

Pools are transparent about whether or not there is an admin key. If not, the pool cannot rebalance; if so, users should be cognizant that the key could allow the pool initiator to size the assets unless it’s a safe on-chain program that doesn’t have that ability.

Admin keys are able to be controlled by on-chain programs as well, which can then be transparent about what they will and won’t do.

## What is further work that could be done on Pools?

Whatever you want! But here are a few known areas for improvement:

- Writing a program to allow a user to initiate a pool with an admin key but have a timelock on any admin actions
  - Note this also has to ensure that pool redemptions aren’t paused during the timelock period
- Writing a program to allow a user to initiate a pool with an admin key with multi-sig control
- Writing a program to allow a user to initiate a pool where the admin key is an on-chain program that only allows trading on Serum DEX markets.
- Writing a program to allow a user to initiate a pool where the admin key is an on-chain program that implements a standard AMM via trading on Serum DEX markets.
- Writing a program that accepts USDC/SOL/SRM and trades it into whatever basket a pool requires for a creation

## What is LQID?

[LQID](https://explorer.solana.com/address/A6aY2ceogBz1VaXBxm1j2eJuNZMRqrWUAnKecrMH85zj) is the governance token of Pools.

Fees from every creation and redemption are governed by LQID (for airdrops, buy/burns, grants, etc.).

There has been no presale of LQID; there is no team or team allocation. 100% of LQID tokens are held by EcoSerum to benefit the Serum ecosystem and SRM token.

There are 500,000,000 LQID tokens, and will never be more.

## Where is the pool program?

You can find the on-chain pool program [here](http://explorer.solana.com/address/WvmTNLpGMVbwJVYztYL4Hnsy82cJhQorxjnnXcRm3b6) (with admin key) and [here](https://explorer.solana.com/address/71JS8f7y7ASMbuuSMCVG7a3qDdcVco2qYD6bMJeZqUCm) (without admin key). You can find the code [here](https://github.com/project-serum/serum-dex/tree/master/pool).
