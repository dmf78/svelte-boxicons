<h1 align="center">Svelte Boxicons</h1>

<p align="center">
<a href="https://shinokada.github.io/svelte-boxicons/">Svelte-Boxicons</a>
</p>

<p align="center">
<a href="https://github.com/sponsors/shinokada" target="_blank"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-boxicons" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/v/svelte-boxicons" alt="npm" height="25"></a>
<a href="https://twitter.com/shinokada" rel="nofollow" target="_blank"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada" height="25"></a>
<a href="https://opensource.org/licenses/MIT" rel="nofollow" target="_blank"><img src="https://img.shields.io/github/license/shinokada/svelte-boxicons" alt="License" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-boxicons" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/dw/svelte-boxicons.svg" alt="npm" height="25"></a>
</p>

1500+ SVG [boxicons](https://github.com/atisawd/boxicons/tree/master) components for Svelte. Svelte-boxicons support major CSS frameworks using the `class` props.

Thank you for considering my open-source package. If you use it in a commercial project, please support me by sponsoring me on GitHub: https://github.com/sponsors/shinokada. Your support helps me maintain and improve this package for the benefit of the community.

<p align="center">
<img width="450" src="https://raw.githubusercontent.com/shinokada/svelte-boxicons/main/static/images/boxicons-450.webp" />
</p>

## Installation

```sh
npm i -D svelte-boxicons
```q

## Icon names

[Icon list](/icon-list.md)

## Icon images

[Icon images](/icon-images.md)

## Usages

In a svelte file:

```html
<script>
  import { BxAbacus } from 'svelte-boxicons';
</script>

<BxAbacus />
```

## Faster compiling

If you need only a few icons from this library in your Svelte app, import them directly. This can optimize compilation speed and improve performance by reducing the amount of code processed during compilation.

```html
<script>
  import BxAbacus from 'svelte-boxicons/BxAbacus.svelte';
</script>

<BxAbacus />
```

If you are a TypeScript user, install **typescript version 5.0.0 or above**.

```sh
pnpm i -D typescript@latest
```

To avoid any complaints from the editor, add `node16` or `nodenext` to `moduleResolution` in your tsconfig.json file.

```json
{
  //...
  "compilerOptions": {
    // ...
    "moduleResolution": "nodenext"
  }
}
```

## Props

- viewBox: string = '0 0 24 24';
- role = 'img';
- strokeWidth = '1.5';
- color = 'currentColor';
- ariaLabel = 'icon file name';

## IDE support

If you are using an LSP-compatible editor, such as VSCode, Atom, Sublime Text, or Neovim, hovering over a component name will display a documentation link, features, props, events, and an example.

## Size

Use the `size` prop to change the size of icons.

```html
<BxAbacus size="40" /> 
```

## CSS HEX Colors

Use the `color` prop to change colors with HEX color code.

```html
<BxAbacus color="#c61515" /> 
```

## CSS framworks suport

Use the `class` prop to change size, colors and add additional css.

Tailwind CSS example:

```html
<BxAbacus class="h-24 w-24 text-blue-700 mr-4" />
```

Bootstrap examples:

```html
<BxAbacus class="position-absolute top-0 px-1" />
```

## Dark mode

If you are using the dark mode on your website with Tailwind CSS, add your dark mode class to the `class` prop.

Let's use `dark` for the dark mode class as an example.

```html
<BxAbacus class="text-blue-700 dark:text-red-500" />
```

## aria-label

All icons have aria-label. For example `BxAbacus` has `aria-label="bx abacus"`.
Use `ariaLabel` prop to modify the `aria-label` value.

```html
<BxAbacus ariaLabel="abacus svg icon" />
```

## Unfocusable icon

If you want to make an icon unfocusable, add `tabindex="-1"`.

```html
<BxAbacus tabindex="-1" />
```

## Events

All icons have the following events:

- on:click
- on:keydown
- on:keyup
- on:focus
- on:blur
- on:mouseenter
- on:mouseleave
- on:mouseover
- on:mouseout

## Passing down other attributes

You can pass other attibutes as well.

```html
<BxAbacus tabindex="0" />
```

## Using svelte:component

```html
<script>
  import { BxAbacus } from 'svelte-boxicons';
</script>

<svelte:component this="{BxAbacus}" />
```

## Using onMount

```html
<script>
  import { BxAbacus } from 'svelte-boxicons';
  import { onMount } from 'svelte';
  const props = {
    size: '50',
    color: '#ff0000'
  };
  onMount(() => {
    const icon = new BxAbacus({ target: document.body, props });
  });
</script>
```

## Import all

Use `import * as Icon from 'svelte-boxicons`.

```html
<script>
  import * as Icon from 'svelte-boxicons';
</script>

<Icon.BxAbacus />

<h1>Size</h1>
<Icon.BxAbacus size="30" />

<h1>CSS HEX color</h1>
<Icon.BxAbacus color="#c61515" size="40" />

<h1>Tailwind CSS</h1>
<Icon.BxAbacus class="text-blue-500" />
```

## Other icons

- [Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)

