---
id: filecoin.js.httpjsonrpcwalletprovider.getnonce
title: HttpJsonRpcWalletProvider.getNonce() method
hide_title: true
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[filecoin.js](./filecoin.js.md) &gt; [HttpJsonRpcWalletProvider](./filecoin.js.httpjsonrpcwalletprovider.md) &gt; [getNonce](./filecoin.js.httpjsonrpcwalletprovider.getnonce.md)

## HttpJsonRpcWalletProvider.getNonce() method

get nonce for address. Note that this method may not be atomic. Use MpoolPushMessage instead.

<b>Signature:</b>

```typescript
getNonce(address: string): Promise<number>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  address | string |  |

<b>Returns:</b>

Promise&lt;number&gt;
