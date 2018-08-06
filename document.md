# JSON RPC API

## JSON-RPC methods

* [getbalance](#getbalance)
* [getbestblockhash](#getbestblockhash)
* [getblock](#getblock)
* [getblockcount](#getblockcount)
* [getblockhash](#getblockhash)
* [getconnectioncount](#getconnectioncount)
* [getrawmempool](#getrawmempool)
* [getrawtransaction](#getrawtransaction)
* [gettxout](#gettxout)
* [getaccountstate](#getaccountstate)
* [getcontractstate](#getcontractstate)
* [getstorage](#getstorage)
* [getpeers](#getpeers)
* [getblocksysfee](#getblocksysfee)
* [sendrawtransaction](#sendrawtransaction)
* [sendtoaddress](#sendtoaddress)
* [submitblock](#submitblock)
* [validateaddress](#validateaddress)
* [invoke](#invoke)
* [invokefunction](#invokefunction)
* [invokescript](#invokescript)




## JSON RPC API Reference


***

#### getbestblockhash

Returns the hash of the highest block of the main chain.


##### Parameters
none

##### Example
```js
// Request
curl -X POST --data '{"jsonrpc":"2.0","method":"getbestblockhash","params":[],"id":64}'

// Result
{
  "id":64,
  "jsonrpc": "2.0",
  "result": "0x6b40aebe942d41b43a8700e40d653934388d79e42155f9d3ba05dd4e2d9d3b55"
}
```

***

#### getblock

Returns block info based on designated hash value

##### Parameters
1. `HASH`, Hash of block.

##### Example
```js
// Request
curl -X POST --data '{"jsonrpc":"2.0","method":"getblock","params":["0xcb40796dbe7d7f9fe4b252f8c436f1bbd9d92159da1a663d4cbaf93f97fef1f6"],"id":71}'

// Result
{
  "id":71,
  "jsonrpc": "2.0",
  "result": "00000000ba36de801556e44ef616e50ec20541856dfe905fe69bfc06a3fa0d10f0fc0d2685a385c53e63c8fb8d9dce6d3eaadb6d2c8220d697af29fb96e113f916ffb07e4a06685baf480000c6c885a2034ad2dcd8365212d403d823360ac264854a1f867903334301fd450140e8b55a549844a1067c9efe15c391f72142e72211feee124bb35d6dfad03b04e0d8f660b812e72fd048a222b84ab600cf651f6289a73b9b1c0973c3a79d08dc7840bc22e1b4533f3f44e8c8a4457e7a90c153fb8c878779a963d1e8c39c3a9d592278430338cdad1470d1f379880dc1f75f850127680a4274bac9aeeaf62164f9604006fc712ae06e4780a3fd1d5d503557cd7b9acc36d48ebd50f051fa953485fc3b7937e51f898f0e578814237eac893000b9fd08d1de22b99fa2551e3e5eff0ada40efe6cd6b9039d209c1f468aa1abd782ff96775614eedea82ee63083eed0966998b2bad4dde73b378644246ed7b8a8f999904d73e1e1603f28712a3936c3aefed403164ebd27bf1d9d23eac014f68676081eec2a70709c3376383aa986f3471acb6feef2f32747a59e2c2f84f9156f1d8147b88b79a0f3664434a926db0bf6b59d8f1552102184ea164ce3728d83ef7e1071b2555a988c2d0bf040c398847907f8d3dc4cee6210326e1b676947dbf5b67d13dcc69e744de9313c352d96b522547c6f0f7dd2b97322103617021c6e3d130e07c10abdb04ba629e3079e904e449d2f4ed0c74f142629a762102af7cbadb23a7cb4a26f0f59b0d38994dd6f0ec486d1ebf9a80202a9101b8133d2103ce0ae9f92d73fa7d2d2fba646afb2607d780c60940485231fa7a83a823b983562102f60736240d5e5a9041895b65685096e63b5bf1c4ce0192a7324b6520f8329ef62102f737a76867f021fad370e32d2e70d703cb422f3ff7e64876a94b4eef10cf30d957ae010000c6c885a200000000"
}

```