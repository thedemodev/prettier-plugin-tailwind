[![npm version](https://badge.fury.io/js/prettier-plugin-tailwind.svg)](https://badge.fury.io/js/prettier-plugin-tailwind)

# Prettier Plugin Tailwind

Sort tailwind classes with Prettier.

**Go from this:**

```html
<div class="z-50 z-10 container  text-left md:text-center justify-center">
	...
</div>
```

**To this:**

```html
<div class="container justify-center text-left z-10 z-50 md:text-center">
	...
</div>
```

This plugin reads your `tailwind.config.js` file to support new keys and classes generated by Tailwind.

## Installation VSCode:

Install Prettier and the plugin into your project locally:

```bash
yarn add --dev prettier prettier-plugin-tailwind
```

_\*supports other IDE's\*_

## Options

These options can be added to your `.prettierrc` file.

---

**twPluginsOrder**

Comma separated order of tailwind plugins to sort classes by.
`""` will use the default order.

```ts
twPluginsOrder: string
```

_Default: `""`_

_Example: `"container,position,inset"`_

---

**twClassesPosition**

Position of component and utility classes. `"as-is"` will allow component classes to be placed between utility classes.

```ts
twClassesPosition: 'components-first' | 'components-last' | 'as-is'
```

_Default: `"components-first"`_

---

**twUnknownClassesPosition**

Position of unknown classes.

```ts
twUnknownClassesPosition: 'start' | 'end'
```

_Default: `"start"`_

---

**twJsxClassAttributes**

Comma separated list of JSX attributes to sort tailwind classes in.

```ts
twJsxClassAttributes:
```

_Default: `"className,tw"`_

---

## Bonus

This plugin also supports [`twin.marco`](https://github.com/ben-rogerson/twin.macro).

## Roadmap

- [x] Add support for configuring plugin order
- [x] Add support for JSX, TSX

## Contributing

**Testing**

Rename `test-tailwind.config.js` to `tailwind.config.js` and run `node ./test.js`.

---

<a href="https://www.buymeacoffee.com/ariseyhun" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>
