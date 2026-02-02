---
id: SequenceOptions
title: SequenceOptions
---

# Interface: SequenceOptions

Defined in: [types.ts:437](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L437)

Options for hotkey sequence matching.

## Extends

- [`HotkeyOptions`](HotkeyOptions.md)

## Properties

### enabled?

```ts
optional enabled: boolean;
```

Defined in: [types.ts:411](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L411)

Whether the hotkey is enabled. Defaults to true

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`enabled`](HotkeyOptions.md#enabled)

***

### eventType?

```ts
optional eventType: "keydown" | "keyup";
```

Defined in: [types.ts:407](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L407)

The event type to listen for. Defaults to 'keydown'

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`eventType`](HotkeyOptions.md#eventtype)

***

### ignoreInputs?

```ts
optional ignoreInputs: boolean;
```

Defined in: [types.ts:413](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L413)

Whether to ignore hotkeys when keyboard events originate from input-like elements (input, textarea, select, contenteditable). Defaults to true

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`ignoreInputs`](HotkeyOptions.md#ignoreinputs)

***

### platform?

```ts
optional platform: "mac" | "windows" | "linux";
```

Defined in: [types.ts:405](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L405)

The target platform for resolving 'Mod'

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`platform`](HotkeyOptions.md#platform)

***

### preventDefault?

```ts
optional preventDefault: boolean;
```

Defined in: [types.ts:401](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L401)

Prevent the default browser action when the hotkey matches

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`preventDefault`](HotkeyOptions.md#preventdefault)

***

### requireReset?

```ts
optional requireReset: boolean;
```

Defined in: [types.ts:409](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L409)

If true, only trigger once until all keys are released. Default: false

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`requireReset`](HotkeyOptions.md#requirereset)

***

### stopPropagation?

```ts
optional stopPropagation: boolean;
```

Defined in: [types.ts:403](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L403)

Stop event propagation when the hotkey matches

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`stopPropagation`](HotkeyOptions.md#stoppropagation)

***

### target?

```ts
optional target: HTMLElement | Document | Window | null;
```

Defined in: [types.ts:415](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L415)

The DOM element to attach the event listener to. Defaults to document.

#### Inherited from

[`HotkeyOptions`](HotkeyOptions.md).[`target`](HotkeyOptions.md#target)

***

### timeout?

```ts
optional timeout: number;
```

Defined in: [types.ts:439](https://github.com/TanStack/keys/blob/main/packages/keys/src/types.ts#L439)

Timeout between keys in milliseconds. Default: 1000
