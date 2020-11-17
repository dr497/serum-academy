---
date: 2020-11-18T00:0:00+00:00
title: Suggestion for building on Serum
weight: 1
---

- For developer resources on Serum and Solana:

  - https://github.com/project-serum/awesome-serum

- For a list of projects built on Serum:

  - https://serum-academy.com/en/built-on-serum/

- RPC servers to use:

  - Default list is https://github.com/project-serum/awesome-serum#rpc-servers
  - Others tend to be less reliable

- If you want to consume Serum market data:

  - Javascript program for on-chain calls: https://github.com/project-serum/serum-js
  - REST server: https://github.com/project-serum/serum-rest-server
  - Bonfida API: https://docs.bonfida.com/#introduction

- Build a mainnet and devnet/testnet toggle and have both; there are differences in performance that are useful to be able to test

  - So useful to have a devnet or testnet version
  - But also useful to have a mainnet version; that way it can be fully tested

- If you need to authenticate transactions, the best thing to do is to use the SPL wallet adapter, which is what e.g. sollet.io users to connect to DEXes

  - Note: you can build in auto-accepting as an option! https://dex.projectserum.com/#/ uses this with sollet.
    - It’s what happens when you click “Automatically approve transactions from https://dex.projectserum.com”
    - If you do, then:
    - For that session
    - As long as the URL is the same
    - As long as the transaction contents match the expected contents (e.g. a DEX order)
  - It will not require clicking ‘accept’
  - This code is in https://github.com/project-serum/sol-wallet-adapter If you want your program to be auto-accepted, submit a PR that adds it!
  - Bonfida, Solong, and others also sometimes connect

- Check that you’re using the same conventions as e.g. sollet for e.g. seed phrase and private key

- Consider composing with existing apps:

  - If your app needs liquidity you can trade on a DEX orderbook or swap
  - If your app needs to mint tokens, consider using https://spl-token-ui.com
  - Generally check out https://serum-academy.com/en/built-on-serum/ and https://github.com/project-serum/awesome-serum for ideas and tools

- For fees going to SRM governance, you can assign to this address if you want

- Something about suggesting that you add your project to awesome-serum, serum-academy, built-on-serum, etc. when it’s ready for users
