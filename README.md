# coding challenge

## instructions

You'll be working in `./packages/app`. The goal is to use mobx stores and display the data in a user interface.
## Data

We'll be using https://mobx.js.org/, and [packages/app/data/asset-list.ts](packages/app/data/asset-list.ts) should be genesis state for a mobx store. 

### mobx `Asset` store methods

* `addAsset(asset: ChainCoin)`

this should add an asset, e.g. `ATOM` or `OSMO` tokens

* `updateAsset(asset: ChainCoin)`

this should update an asset, `denom_units`, `base`, `logo_URIs`, etc.

* `removeAsset(asset: ChainCoin)`

### mobx `Pool` store methods

* `addPool(asset1: ChainCoin, asset2: ChainCoin)` 

This should add a pool of two assets. 

## User Interface

A react next.js page exists at [packages/app/pages/index.tsx](packages/app/pages/index.tsx)

Components are already built using https://chakra-ui.com/ — it's optional if you want to add new UI.

```
cd ./packages/app/
yarn dev
```

A pool list UI is already ready, but is hard-coded to use `asset-list`. It should be hooked up to the mobx store instead.


Update `ListPools` to take react `props` to connect to the mobx store. When you call `addPool`, it should add pools to the UI. 

The pools component is here: [packages/app/components/pools-list.tsx](packages/app/components/pools-list.tsx)

## Note on data input

you can optionally make a form, or, you can use code to seed the mobx store and manually call `addPool`.

# setup

```
yarn
yarn bootstrap
```

## next

```
cd ./packages/app
yarn dev
```
