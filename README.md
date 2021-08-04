# ERC20

## Deployment:
```console
$ apt install nodejs
```
```console
$ apt install npm
```
```console
$ apt install git
```
```console
$ npm install -g truffle
```
```console
$ cd truffle
```
```console
$ truffle init
```
```console
$ cd contracts/
```
```console
$ git clone https://github.com/JewEllerrr/ERC20.git
```
```console
$ mv ERC20/* .
```
```console
$ rm -rf ERC20
```
```console
$ cd ../migrations
```
```console
$ nano 2_deploy_migration.js
```
Paste:
```js
const Token = artifacts.require("TDToken.sol");
module.exports = function (deployer) {
deployer.deploy(Token);
};
```
Save file.
```console
$ cd ..
```
```console
$ npm install truffle-hdwallet-provider
```
```console
$ nano truffle-config.js
```
Uncomment and set "version" of your compiler (in my case it is 0.5.0), then configure your "network" by this tutorial (https://andresaaap.medium.com/how-to-deploy-a-smart-contract-on-a-public-test-network-rinkeby-using-infura-truffle-8e19253870c4). Save changes.
```console
$ truffle migrate --network <name_of_network>
```

## Usage:

```console
$ truffle console --network <name_of_network>
```
