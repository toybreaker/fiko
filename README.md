# [FIKO 🐸 CSS <small>FRAMEWORK</small>.](https://fiko.rokma.rocks/) [![Netlify Status](https://api.netlify.com/api/v1/badges/68612997-fe61-4776-80d5-9edd46c5a331/deploy-status)](https://app.netlify.com/sites/fikocss/deploys)

## IMPORT IT FROM NPM. LINK IT IN YOUR APP. BOOM. DONE!

### FIKO DELIVERS A SLIM CSS STARTER, BATTERIES INCLUDED.

It's contained, layered, up-to-date (2024). Uses dynamic units responsivity, semantic html and it's almost classless. VERY 🐸 FIKO!

🐸 GREAT STYLES WITH JUST ONE CSS FILE (46 kb uncompressed!).
🐸 ZERO CONFIG DX, RESPONSIVE, VARIABLE EVERYTHING.
🐸 LIGHT OR DARK AUTOMATIC MODE.
🐸 FIKO USES NATIVE HTML, MIN NORMALISE, LAYERS, GRID, CONTAINER QUERIES.
🐸 FIKO LET YOU WRITE YOUR OWN CLASSES.
🐸 FIKO LOW VERBOSITY LET US DEVs STAY SANE.

.

# 🫵 WAY TO USE IT (actually, don't use it yet, WIP v0.13.0)

.

## Usage: **Install**

```shell
pnpm i fiko
```

## Usage: **Import**

```css
@import 'node_modules/fiko/fiko.css';
```

then in the page `<head>`:

```html
/* tell browser that page supports light & dark modes */
<meta name="color-scheme" content="light dark" />
<link
  rel="stylesheet"
  href="node_modules/fiko/package/fiko.css"
/>
```

Or

## Usage: **Download**

[Download FIKO](https://github.com/TOYBREAKER/fiko/fiko.zip) and link `/fiko.css` it in the `<head>` of your website.

```html
/* tell browser that page supports light & dark modes */
<meta name="color-scheme" content="light dark" />
<link rel="stylesheet" href="fiko.css" />
```

Or

## Usage: **Astro**

```astro
import 'fiko.css';
```

Or

## Usage: **HTML**

Put your custom styles on top of fiko, make sure to not use `!important` in your css cos it might break things.

```shell
import 'fiko' from 'path/to/fiko.css'
import 'my_custom_style' from 'path/to/my_custom_style.css'
```

Or probably also as show here:

```html
<link
  rel="stylesheet"
  href="https://raw.githubusercontent.com/toybreaker/fiko/main/package/fiko.css"
/>
```

Most use case will need some custom, brand related styles...

## Usage: **CUSTOM CSS ON TOP OF FIKO**

Write your `my_custom_style.css` you can leverage the existing `fiko layers`, just mind the order`.

```css
/* ||| Layer Order Declaration ||| */
@layer reset, root, base, roles, toggle, containers, components, classes;
```

### WHY?

The goal here is to reduce specificity born problems, by isolating rules.
Refer to the code comments right inside `fiko.css` to decide where to put your rules. I'd say you probably go something like this:

```css
@layer components {
  .button {
    color: green;
  }
  .call-to-action {
    font-size: 4ch;
    font-weight: 100;
    border: 1px solid pink;
  }
}
```

or

```css
@layer root {
  :root {
    --color-white: #7fffd4;
    --color-black: #222222;
  }
}
```

or, if you want to change just one color of the 4 can go like this:

```css
@layer root {
  :root {
    --dark-mode: var(--color-darkblue);
  }
}
```

or define it just for one page, and just the dark color, like this:

```html
<head>
  ...
  <style>
    @layer root {
      :root {
        --color-darkblue: darkblue;
        --dark-mode: var(--color-darkblue);
      }
    }
  </style>
</head>
```

Generally if you are unsure just put them into un an unnamed, anonymous layer:

```css
@layer {
  p {
    margin: 0;
  }
}
```

## Use [Check colour contrast](https://colourcontrast.cc/) | [Devs here!](https://github.com/Pushedskydiver/Colour-Contrast-Checker)

.

# 🫵 DEVELOP

.

## UPGRADE

```shell
# Start by LIVING IN THE FUTURE:
pnpm upgrade
```

## SEE INCLUDED SCRIPTS

```shell
# See ALL THE AVAILABLE SCRIPTS like this:
cat package.json
```

## LAUNCH NEW PROJECT

```shell
# FIKO ASTRO START, PASTE this one:
pnpm create astro@latest && pnpm add fiko
```

## ADD TO EXISTING PROJECT

```shell
# Add to EXISTING PROJECT using NPM:
npm astro add fiko
```

## FRONTEND [DEMO PAGE](https://fiko.rokma.rocks)

Fiko comes with a demo page, useful to test and dev.
Use Browsersync (install it system wide, it's very useful!)

```shell
# 🐲 DRY RECURRING START
browser-sync start --s 'package' --files 'package' --no-inject-changes
```

or:

```shell
cd package && browser-sync start --s
```

Now you have an auto-reload server whatching all files in 'package'. You'd see this in your terminal:

```shell
Local: http://localhost:3000
External: http://192.168.100.103:3000
```

.

## NPM CAVEAT

Sometimes you need to solve dep's issues. This helps a lot, many times:

```shell
pnpm install --install-strategy=nested
```

`--install-strategy=nested`,
Formerly `legacy-bundling`,
instead of hoisting package installs in node_modules,
installs packages in the same manner that they are depended on.

NOTE: This may cause very deep directory structures and duplicate package installs as there is no de-duplicating.

.

# LIMITATIONS

FIKO can be used without custom CSS for quick or small projects. However, it’s designed to provide a starting point, like a “reset CSS on steroids”.

Developing with `fiko.css` require modern CSS knowledge to add any custom look.

### BROWSER SUPPORT

FIKO is designed and tested for the latest stable Chrome, Firefox, Edge, and Safari releases. It does NOT support any version of IE, including IE 11.

### COPYRIGHT AND LICENSE

Licensed under the [MIT License](https://github.com/toybreaker/fiko/blob/master/LICENSE.md).

This slim starter was develop to scratch my own needs and it's inspired by classless css framework such as [PICOCSS](https://github.com/picocss/pico), [WATER](https://github.com/kognise/water.css), [CSSBED](https://www.cssbed.com/), by [TOYBREAKER](https://github.com/toybreaker/)

.

2do:

- finish container queries grid
- dialog
- more tests
- footer links
- .

# CHANGELOG

## fiko@0.11.0 | Small improvements

Fixed:

- .container, now w/ media queries and side space.
- root text size
- headings now width: 100%
- no heading uppercase, moved to .uppercase class

## fiko@0.10.0 | Small fixes

Added meta def in page head to tell browser that page supports dark and light modes:

```
<meta name="color-scheme" content="light dark" />
```

Dropped modules (temporarily). Need to check if they are actually needed and eventually will be resumed later on.

## fiko@0.9.0 | Fine tuning

Improved container queries

## fiko@0.6.0 | Use the platform

### Some new layers:

```css
@layer reset, root, base, roles, toggle, containers, components, classes;
```

### Invert color-scheme utility class:

```css
.invert {
  filter: invert(1);
}
```

### Color constants:

```css
/* COLOURS FOR LIGHT/DARK MODES */
/* '--alpha' CAN BE REDECLARED AS NEEDED */
--alpha: 1;
--color-white: rgba(255, 255, 255, var(--alpha));
--color-black: rgba(0, 0, 0, var(--alpha));

/* MODE-INDIPENDENT CONSTANT COLOURS */
/* When elements need consistency, not switching colors. */
--color-light: var(--color-white);
--color-dark: var(--color-black);
```

### Color mode variables, Set the current varialiable and auto-get the derived ones.

```css
/* Initial styles assuming light theme */
body[data-theme='light'] {
  /* set the CURRENT colours: */
  --currentBG: var(--color-white);
  --currentTXT: var(--color-black);
  --currentTXT50: rgba(0, 0, 0, 0.5);
  --currentV: var(--icon-chevron-black);
  /* DERIVED: apply the CURRENT colours: */
  background-color: var(--currentBG);
  color: var(--currentTXT);
}
```

## fiko@0.5.0 | Restart with moder tech

Restart from ZERO.
Css Only. With variables, nesting, layers, dvh, dvw, oklch, etc..
2023 Platform. Let's Use it, Zod-damm-it!
New slim structure:

```shell
package/
|- fiko.css
|- index.html
```

## fiko@0.4.1 | DEAD END

Dont fix a broken house, It's faster to make a new one. Crucible moment. SCSS I love you but we gotta move on baby, there are new ways out there. New vehicle, fresh start.
