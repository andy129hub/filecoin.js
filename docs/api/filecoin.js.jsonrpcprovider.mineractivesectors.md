---
id: filecoin.js.jsonrpcprovider.mineractivesectors
title: JsonRpcProvider.minerActiveSectors() method
hide_title: true
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[filecoin.js](./filecoin.js.md) &gt; [JsonRpcProvider](./filecoin.js.jsonrpcprovider.md) &gt; [minerActiveSectors](./filecoin.js.jsonrpcprovider.mineractivesectors.md)

## JsonRpcProvider.minerActiveSectors() method

returns info about sectors that a given miner is actively proving.

<b>Signature:</b>

```typescript
minerActiveSectors(address: string, tipSetKey?: TipSetKey): Promise<ChainSectorInfo[]>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  address | string |  |
|  tipSetKey | TipSetKey |  |

<b>Returns:</b>

Promise&lt;ChainSectorInfo\[\]&gt;