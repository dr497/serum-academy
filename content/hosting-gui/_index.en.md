---
title: How to host a GUI
weight: 8
<!-- chapter: true -->
---

## Create your own GUI

### Serum GUI

You will find the official repository of Serum DEX UI here: [https://github.com/project-serum/serum-dex-ui](https://github.com/project-serum/serum-dex-ui). This provides you with everything you need to start your own Serum GUI.

Once you have forked the repository, you can run a local environment by running:

```bash
yarn start
```

### Customizing

The Serum DEX UI uses [React](https://reactjs.org) and [Ant Design](https://ant.design) UI library. To learn how to customize it, refer to their [official guide](https://ant.design/docs/react/customize-theme)

### Collecting fees

Serum allows you to collect 20% of the fees for the orders made on your GUI. In order to collect the fees, you need to modify the `.env` file that looks like this:

```bash
REACT_APP_USDT_REFERRAL_FEES_ADDRESS=''
REACT_APP_USDC_REFERRAL_FEES_ADDRESS=''
```

To collect fees enter your USDT **SPL** and USD **SPL** addresses, for example:

```bash
REACT_APP_USDT_REFERRAL_FEES_ADDRESS=9EscMUvizE1ThHWuWQgs8siDz4r54yVxhZDub3ihWQAX
REACT_APP_USDC_REFERRAL_FEES_ADDRESS=9GiKG99ngtKzhQcNXtHokuhx5gk7ftKfrmKtrybHFNa1
```

### Setting your own domain name

The `package.json` file contains a field called `homepage`, change it to your name domain.

## Hosting

There are different solutions to host your GUI. You can host it for free on Github Pages or host it on your own server.

### Github Pages

This is the easiest way of hosting and deploying a GUI, you simply have to use the following command to deploy your GUI

```bash
yarn deploy
```

The GUI will then be hosted on the `gh-pages` branch of your Github repository.

### Hosting on your own server

Alternatively, you can host your GUI on your own server and use Nginx for instance to serve it. To create the production build run

```bash
yarn build
```

The build will be created in the `build` folder of the working directory.
