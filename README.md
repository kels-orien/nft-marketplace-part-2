# nft-marketplace-part-1
A [tutorial](https://dev.to/kels_orien/building-a-nft-market-place-with-near-protocol-and-reactjs-1bpi-temp-slug-8479008?preview=3d2f12f601ff1a901cc45bafa9ca1649cdab8462fd413f383af74216df80c6c5c405cff9d102e5bfa272617298fb75f7a039b2d66a67fa347ec9d28e) of an NFT Market Place built using Near Protocol and React.js Part 2.

#### Preview
![alt-text](https://res.cloudinary.com/dofiasjpi/image/upload/v1653483048/near-tutorial-nfts/nft-marketplace-2.png)


#### To run this app locally, follow below steps:

##### Clone using command line interface:
```
git clone https://github.com/kels-orien/nft-marketplace-part-2.git
```

##### Create wallet testnet account
open [wallet testnet account](wallet.testnet.near.org/)


##### From the `market_contract` folder/directory using command CLI, login to near wallet account


`near login`


##### Build the contract
From `market_contract` directory using CLI:

For Windows users:

```
/build.bat
```

For Mac and Linux users:

```
/build.sh
```

##### Create a  Market subaccount

To create subaccount from `market_contract` directory via CLI use command:

```
near create-account  market_contract.youraccountname.testnet --masterAccount youraccountname.testnet


```

##### Deploy the contract
```
near deploy market_contract.kelsacc.testnet --wasmFile res/market_contract.wasm

```





##### Edit contract name

Change the `youraccountname` part of the `MARKET_CONTRACT_NAME` constant in `config.js` file to your own account name.


### Initialize Your contract

 To initialize our market contract from CLI:

```
near call market_contract.youraccountname.testnet new '{"owner_id": "nft-contract.youraccountname.testnet"}' --accountId youraccountname.testnet

```

##### Install packages for frontend

Go to root directory `nft-marketplac-part-1` using CLI and install packages:

```
cd ..
npm install

```

##### Launch frontend

```
npm start

```



