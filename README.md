# ERC20

##### deployment:
0) apt install nodejs
1) apt install npm
2) apt install git
3) npm install -g truffle
4) cd truffle
5) truffle init
6) cd contracts/
7) git clone https://github.com/JewEllerrr/ERC20.git
8) mv ERC20/* .
9) rm -rf ERC20
10) cd ../migrations
11) nano 2_deploy_migration.js --> const Token = artifacts.require("TDToken.sol");
                                        module.exports = function (deployer) {
                                          deployer.deploy(Token);
                                        };
12) cd ..
13) npm install truffle-hdwallet-provider
14) nano truffle-config.js --> uncomment and set "version" of your compiler (in my case this is 0.5.0), then configure your "network" by this tutorial (https://andresaaap.medium.com/how-to-deploy-a-smart-contract-on-a-public-test-network-rinkeby-using-infura-truffle-8e19253870c4)
15) truffle migrate --network <name_of_network>


##### usage:
$ truffle console --network <name_of_network>
