# SchellingPoint2022
Schelling Point Hackathon 


## Fluence P2P setup

APIs exposed via the P2P network

OpenSea [https://testnets-api.opensea.io/api/v1/assets?order_direction=desc&offset=0&limit=3](https://testnets-api.opensea.io/api/v1/assets?order_direction=desc&offset=0&limit=3)

Rarible [https://ethereum-api.rarible.org/v0.1/nft/items/all?size=5](https://ethereum-api.rarible.org/v0.1/nft/items/all?size=5)

## P2P node details


```NFT_MARKETPLACE_NODE_PEER_ID ?= "12D3KooWFEwNWcHqi9rtsmDhsYcDbRUCDXH84RC4FW6UfsFWaoHi"```


```NFT_MARKETPLACE_SERVICE_ID ?= "7f792f0b-8e9b-4b6d-90f7-bd6461e84d1d"```




## Functions available on the P2P node
```
data NFTEcho:
  msg: string
  reply: string

service MarketplaceService:
  opensea_fetch(page: i32, page_size: i32) -> NFTEcho
  rarible_fetch(continuation: string, size: i32) -> NFTEcho
  ```
