[Bot Builder SDK](../README.md) > [BotStateSet](../classes/botbuilder.botstateset.md)



# Class: BotStateSet

## Implements

* `any`

## Index

### Constructors

* [constructor](botbuilder.botstateset.md#constructor)


### Methods

* [onProcessRequest](botbuilder.botstateset.md#onprocessrequest)
* [readAll](botbuilder.botstateset.md#readall)
* [use](botbuilder.botstateset.md#use)
* [writeAll](botbuilder.botstateset.md#writeall)



---
## Constructors
<a id="constructor"></a>


### ⊕ **new BotStateSet**(...middleware: *[BotState](botbuilder.botstate.md)[]*): [BotStateSet](botbuilder.botstateset.md)


*Defined in [libraries/botbuilder-core-extensions/lib/botStateSet.d.ts:12](https://github.com/Microsoft/botbuilder-js/blob/f986273/libraries/botbuilder-core-extensions/lib/botStateSet.d.ts#L12)*



Creates a new BotStateSet instance.


**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| middleware | [BotState](botbuilder.botstate.md)[]   |  Zero or more BotState plugins to register. |





**Returns:** [BotStateSet](botbuilder.botstateset.md)

---


## Methods
<a id="onprocessrequest"></a>

###  onProcessRequest

► **onProcessRequest**(context: *[BotContext](botbuilder.botcontext.md)*, next: *`function`*): `Promise`.<`void`>



*Defined in [libraries/botbuilder-core-extensions/lib/botStateSet.d.ts:18](https://github.com/Microsoft/botbuilder-js/blob/f986273/libraries/botbuilder-core-extensions/lib/botStateSet.d.ts#L18)*



**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| context | [BotContext](botbuilder.botcontext.md)   |  - |
| next | `function`   |  - |





**Returns:** `Promise`.<`void`>





___

<a id="readall"></a>

###  readAll

► **readAll**(context: *[BotContext](botbuilder.botcontext.md)*, force?: *`undefined`⎮`true`⎮`false`*): `Promise`.<[StoreItem](../interfaces/botbuilder.storeitem.md)[]>



*Defined in [libraries/botbuilder-core-extensions/lib/botStateSet.d.ts:30](https://github.com/Microsoft/botbuilder-js/blob/f986273/libraries/botbuilder-core-extensions/lib/botStateSet.d.ts#L30)*



Calls `BotState.read()` on all of the BotState plugins in the set. This will trigger all of the plugins to read in their state in parallel.


**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| context | [BotContext](botbuilder.botcontext.md)   |  Context for current turn of conversation with the user. |
| force | `undefined`⎮`true`⎮`false`   |  (Optional) If `true` the cache will be bypassed and the state will always be read in directly from storage. Defaults to `false`. |





**Returns:** `Promise`.<[StoreItem](../interfaces/botbuilder.storeitem.md)[]>





___

<a id="use"></a>

###  use

► **use**(...middleware: *[BotState](botbuilder.botstate.md)[]*): `this`



*Defined in [libraries/botbuilder-core-extensions/lib/botStateSet.d.ts:23](https://github.com/Microsoft/botbuilder-js/blob/f986273/libraries/botbuilder-core-extensions/lib/botStateSet.d.ts#L23)*



Registers `BotState` middleware plugins with the set.


**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| middleware | [BotState](botbuilder.botstate.md)[]   |  One or more BotState plugins to register. |





**Returns:** `this`





___

<a id="writeall"></a>

###  writeAll

► **writeAll**(context: *[BotContext](botbuilder.botcontext.md)*, force?: *`undefined`⎮`true`⎮`false`*): `Promise`.<`void`>



*Defined in [libraries/botbuilder-core-extensions/lib/botStateSet.d.ts:37](https://github.com/Microsoft/botbuilder-js/blob/f986273/libraries/botbuilder-core-extensions/lib/botStateSet.d.ts#L37)*



Calls `BotState.write()` on all of the BotState plugins in the set. This will trigger all of the plugins to write out their state in parallel.


**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| context | [BotContext](botbuilder.botcontext.md)   |  Context for current turn of conversation with the user. |
| force | `undefined`⎮`true`⎮`false`   |  (Optional) if `true` the state will always be written out regardless of its change state. Defaults to `false`. |





**Returns:** `Promise`.<`void`>





___

