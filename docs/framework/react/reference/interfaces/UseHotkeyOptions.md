---
id: UseHotkeyOptions
title: UseHotkeyOptions
---

# Interface: UseHotkeyOptions

Defined in: [useHotkey.ts:12](https://github.com/TanStack/hotkeys/blob/main/packages/react-hotkeys/src/useHotkey.ts#L12)

## Extends

- `Omit`\<`HotkeyOptions`, `"target"`\>

## Properties

### target?

```ts
optional target: 
  | HTMLElement
  | RefObject<HTMLElement | null>
  | Document
  | Window
  | null;
```

Defined in: [useHotkey.ts:18](https://github.com/TanStack/hotkeys/blob/main/packages/react-hotkeys/src/useHotkey.ts#L18)

The DOM element to attach the event listener to.
Can be a React ref, direct DOM element, or null.
Defaults to document.
