---
id: HotkeyManager
title: HotkeyManager
---

# Class: HotkeyManager

Defined in: [manager.ts:40](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L40)

Singleton manager for hotkey registrations.

This class provides a centralized way to register and manage keyboard hotkeys.
It uses a single event listener for efficiency, regardless of how many hotkeys
are registered.

## Example

```ts
const manager = HotkeyManager.getInstance()

const unregister = manager.register('Mod+S', (event, context) => {
  console.log('Save triggered!')
}, { preventDefault: true })

// Later, to unregister:
unregister()
```

## Methods

### destroy()

```ts
destroy(): void;
```

Defined in: [manager.ts:459](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L459)

Destroys the manager and removes all listeners.

#### Returns

`void`

***

### getRegistrationCount()

```ts
getRegistrationCount(): number;
```

Defined in: [manager.ts:440](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L440)

Gets the number of registered hotkeys.

#### Returns

`number`

***

### isRegistered()

```ts
isRegistered(hotkey): boolean;
```

Defined in: [manager.ts:447](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L447)

Checks if a specific hotkey is registered.

#### Parameters

##### hotkey

[`Hotkey`](../type-aliases/Hotkey.md)

#### Returns

`boolean`

***

### register()

```ts
register(
   hotkey, 
   callback, 
   options): () => void;
```

Defined in: [manager.ts:89](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L89)

Registers a hotkey handler.

#### Parameters

##### hotkey

[`Hotkey`](../type-aliases/Hotkey.md)

The hotkey string to listen for

##### callback

[`HotkeyCallback`](../type-aliases/HotkeyCallback.md)

The function to call when the hotkey is pressed

##### options

[`HotkeyOptions`](../interfaces/HotkeyOptions.md) = `{}`

Options for the hotkey behavior

#### Returns

A function to unregister the hotkey

```ts
(): void;
```

##### Returns

`void`

***

### getInstance()

```ts
static getInstance(): HotkeyManager;
```

Defined in: [manager.ts:64](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L64)

Gets the singleton instance of HotkeyManager.

#### Returns

`HotkeyManager`

***

### resetInstance()

```ts
static resetInstance(): void;
```

Defined in: [manager.ts:74](https://github.com/TanStack/keys/blob/main/packages/keys/src/manager.ts#L74)

Resets the singleton instance. Useful for testing.

#### Returns

`void`
