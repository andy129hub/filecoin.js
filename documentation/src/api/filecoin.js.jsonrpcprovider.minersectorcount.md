---
id: filecoin.js.jsonrpcprovider.minersectorcount
title: JsonRpcProvider.minerSectorCount() method
hide_title: true
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[filecoin.js](./filecoin.js.md) &gt; [JsonRpcProvider](./filecoin.js.jsonrpcprovider.md) &gt; [minerSectorCount](./filecoin.js.jsonrpcprovider.minersectorcount.md)

## JsonRpcProvider.minerSectorCount() method

returns the number of sectors in a miner's sector set and proving set

<b>Signature:</b>

```typescript
minerSectorCount(address: Address, tipSetKey?: TipSetKey): Promise<MinerSectors>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  address | Address |  |
|  tipSetKey | TipSetKey |  |

<b>Returns:</b>

Promise&lt;MinerSectors&gt;