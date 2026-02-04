---
id: HotkeyRegistrationHandle
title: HotkeyRegistrationHandle
---

# Interface: HotkeyRegistrationHandle

Defined in: [types.ts:492](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L492)

A handle returned from HotkeyManager.register() that allows updating
the callback and options without re-registering the hotkey.

This pattern is similar to TanStack Pacer's Debouncer, where the function
and options can be synced on every render to avoid stale closures.

## Example

```ts
const handle = manager.register('Mod+S', callback, options)

// Update callback without re-registering (avoids stale closures)
handle.callback = newCallback

// Update options without re-registering
handle.setOptions({ enabled: false })

// Check if still active
if (handle.isActive) {
  // ...
}

// Unregister when done
handle.unregister()
```

## Properties

### callback

```ts
callback: HotkeyCallback;
```

Defined in: [types.ts:503](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L503)

The callback function. Can be set directly to update without re-registering.
This avoids stale closures when the callback references React state.

***

### id

```ts
readonly id: string;
```

Defined in: [types.ts:494](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L494)

Unique identifier for this registration

***

### isActive

```ts
readonly isActive: boolean;
```

Defined in: [types.ts:512](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L512)

Check if this registration is still active (not unregistered)

***

### setOptions()

```ts
setOptions: (options) => void;
```

Defined in: [types.ts:509](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L509)

Update options (merged with existing options).
Useful for updating `enabled`, `preventDefault`, etc. without re-registering.

#### Parameters

##### options

`Partial`\<[`HotkeyOptions`](HotkeyOptions.md)\>

#### Returns

`void`

***

### unregister()

```ts
unregister: () => void;
```

Defined in: [types.ts:497](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L497)

Unregister this hotkey

#### Returns

`void`
