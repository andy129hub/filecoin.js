## API Report File for "filecoin.js"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { BigNumber } from 'bignumber.js';
import { EventEmitter } from 'events';
import { FilecoinSnapApi } from '@nodefactory/filsnap-types';

// Warning: (ae-forgotten-export) The symbol "Connector" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export class HttpJsonRpcConnector extends EventEmitter implements Connector {
    constructor(options: string | JsonRpcConnectionOptions);
    // (undocumented)
    connect(): Promise<any>;
    // (undocumented)
    disconnect(): Promise<any>;
    // (undocumented)
    on(event: 'connected' | 'disconnected', listener: (...args: any[]) => void): this;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcConnectionOptions" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    protected options: string | JsonRpcConnectionOptions;
    // (undocumented)
    protected reqId: number;
    // Warning: (ae-forgotten-export) The symbol "RequestArguments" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    request(req: RequestArguments): Promise<unknown>;
    // (undocumented)
    token?: string | undefined;
    // (undocumented)
    url: string;
}

// Warning: (ae-forgotten-export) The symbol "WalletProvider" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export class HttpJsonRpcWalletProvider implements WalletProvider {
    constructor(connector: Connector);
    // Warning: (ae-forgotten-export) The symbol "MessagePartial" needs to be exported by the entry point index.d.ts
    createMessage(message: MessagePartial): Promise<Message>;
    deleteWallet(address: string): Promise<any>;
    estimateMessageGas(message: Message): Promise<Message>;
    estimateMessageGasFeeCap(message: Message, nblocksincl: number): Promise<string>;
    estimateMessageGasLimit(message: Message): Promise<number>;
    estimateMessageGasPremium(nblocksincl: number, sender: string, gasLimit: number): Promise<string>;
    getAccounts(): Promise<string[]>;
    getBalance(address: string): Promise<any>;
    getDefaultAccount(): Promise<string>;
    getNonce(address: string): Promise<number>;
    hasWallet(address: string): Promise<any>;
    newAccount(type?: number): Promise<string>;
    // (undocumented)
    release(): Promise<any>;
    // Warning: (ae-forgotten-export) The symbol "Message" needs to be exported by the entry point index.d.ts
    // Warning: (ae-forgotten-export) The symbol "SignedMessage" needs to be exported by the entry point index.d.ts
    sendMessage(msg: Message): Promise<SignedMessage>;
    // Warning: (ae-forgotten-export) The symbol "Cid" needs to be exported by the entry point index.d.ts
    sendSignedMessage(msg: SignedMessage): Promise<Cid>;
    setDefaultAccount(address: string): Promise<undefined>;
    // Warning: (ae-forgotten-export) The symbol "Signature" needs to be exported by the entry point index.d.ts
    sign(data: string | ArrayBuffer): Promise<Signature>;
    signMessage(msg: Message): Promise<SignedMessage>;
    verify(address: string, data: string | ArrayBuffer, sign: Signature): Promise<boolean>;
    // Warning: (ae-forgotten-export) The symbol "KeyInfo" needs to be exported by the entry point index.d.ts
    walletExport(address: string): Promise<KeyInfo>;
    walletImport(keyInfo: KeyInfo): Promise<string>;
}

// @public (undocumented)
export class LotusClient {
    constructor(connector: Connector);
    // Warning: (ae-forgotten-export) The symbol "JsonRpcAuthMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    auth: JsonRpcAuthMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcChainMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    chain: JsonRpcChainMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcClientMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    client: JsonRpcClientMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcCommonMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    common: JsonRpcCommonMethodGroup;
    // (undocumented)
    conn: Connector;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcMinerMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    miner: JsonRpcMinerMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcMPoolMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    mpool: JsonRpcMPoolMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcMsigMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    msig: JsonRpcMsigMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcNetMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    net: JsonRpcNetMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcPaychMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    paych: JsonRpcPaychMethodGroup;
    // (undocumented)
    release(): Promise<any>;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcStateMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    state: JsonRpcStateMethodGroup;
    // Warning: (ae-forgotten-export) The symbol "JsonRpcSyncMethodGroup" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    sync: JsonRpcSyncMethodGroup;
}

// @public (undocumented)
export class LightWalletProvider extends HttpJsonRpcWalletProvider {
    constructor(connector: Connector);
    // (undocumented)
    createLightWallet(password: string): Promise<string>;
    // (undocumented)
    getAccounts(): Promise<string[]>;
    // (undocumented)
    getDefaultAccount(): Promise<string>;
    // (undocumented)
    getSigner(): LightWalletSigner;
    // Warning: (ae-forgotten-export) The symbol "Keystore" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    keystore: Keystore;
    // (undocumented)
    loadLightWallet(encryptedWallet: string): void;
    // (undocumented)
    prepareToSave(): string;
    // (undocumented)
    recoverLightWallet(mnemonic: string, password: string): Promise<void>;
    // (undocumented)
    sendMessage(msg: Message, password?: string): Promise<SignedMessage>;
    // (undocumented)
    sign(data: string | ArrayBuffer): Promise<Signature>;
    // (undocumented)
    signMessage(msg: Message, password?: string): Promise<SignedMessage>;
    // (undocumented)
    verify(address: string, data: string | ArrayBuffer, sign: Signature): Promise<boolean>;
}

// Warning: (ae-forgotten-export) The symbol "Signer" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export class LightWalletSigner implements Signer {
    constructor(keystore: Keystore);
    // (undocumented)
    getDefaultAccount(): Promise<string>;
    // (undocumented)
    sign(message: Message, password?: string): Promise<SignedMessage>;
}

// @public (undocumented)
export class MetamaskSigner implements Signer {
    constructor(filecoinApi: FilecoinSnapApi);
    // (undocumented)
    getDefaultAccount(): Promise<string>;
    // (undocumented)
    sign(message: Message): Promise<SignedMessage>;
}

// @public (undocumented)
export class MetamaskSnapHelper {
    constructor(connection: JsonRpcConnectionOptions);
    // (undocumented)
    error: string | undefined;
    // (undocumented)
    filecoinApi: FilecoinSnapApi | undefined;
    // (undocumented)
    installFilecoinSnap(): Promise<any>;
    }

// @public (undocumented)
export class MetamaskWalletProvider extends HttpJsonRpcWalletProvider {
    constructor(connector: Connector, filecoinApi: FilecoinSnapApi);
    // (undocumented)
    getAccounts(): Promise<string[]>;
    // (undocumented)
    getDefaultAccount(): Promise<string>;
    // (undocumented)
    getSigner(): MetamaskSigner;
    // (undocumented)
    sendMessage(msg: Message): Promise<SignedMessage>;
    // (undocumented)
    sign(data: string | ArrayBuffer): Promise<Signature>;
    // (undocumented)
    signMessage(msg: Message): Promise<SignedMessage>;
    // (undocumented)
    verify(address: string, data: string | ArrayBuffer, sign: Signature): Promise<boolean>;
}

// @public (undocumented)
export class MnemonicSigner implements Signer {
    // Warning: (ae-forgotten-export) The symbol "StringGetter" needs to be exported by the entry point index.d.ts
    constructor(mnemonic: string | StringGetter, password: string | StringGetter, path?: string);
    // (undocumented)
    getDefaultAccount(): Promise<string>;
    // (undocumented)
    sign(message: Message): Promise<SignedMessage>;
}

// @public (undocumented)
export class MnemonicWalletProvider extends HttpJsonRpcWalletProvider {
    constructor(connector: Connector, mnemonic: string | StringGetter, password: string | StringGetter, path?: string);
    // (undocumented)
    getAccounts(): Promise<string[]>;
    // (undocumented)
    getDefaultAccount(): Promise<string>;
    // (undocumented)
    getSigner(): MnemonicSigner;
    // (undocumented)
    sendMessage(msg: Message): Promise<SignedMessage>;
    // (undocumented)
    sign(data: string | ArrayBuffer): Promise<Signature>;
    // (undocumented)
    signMessage(msg: Message): Promise<SignedMessage>;
    // (undocumented)
    verify(address: string, data: string | ArrayBuffer, sign: Signature): Promise<boolean>;
}

// @public (undocumented)
export class WsJsonRpcConnector extends EventEmitter implements Connector {
    // Warning: (ae-forgotten-export) The symbol "WebSocketConnectionOptions" needs to be exported by the entry point index.d.ts
    constructor(options: WebSocketConnectionOptions);
    // (undocumented)
    closeSubscription(subscriptionId: string): Promise<void>;
    // (undocumented)
    connect(): Promise<any>;
    // (undocumented)
    disconnect(): Promise<any>;
    // Warning: (ae-forgotten-export) The symbol "SubscriptionId" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    on(event: 'connected' | 'disconnected' | 'error' | SubscriptionId, listener: (...args: any[]) => void): this;
    // (undocumented)
    request(args: RequestArguments): Promise<any>;
    // (undocumented)
    token?: string;
    // (undocumented)
    url: string;
    }


// (No @packageDocumentation comment for this package)

```
