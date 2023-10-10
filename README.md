[![Netlify Status](https://api.netlify.com/api/v1/badges/68612997-fe61-4776-80d5-9edd46c5a331/deploy-status)](https://app.netlify.com/sites/fikocss/deploys)

# [FIKO 🐸 CSS <small>FRAMEWORK</small>.](https://fiko.rokma.rocks/)

.

Full zero config DX. Import it from NPM. Link it in yor framework. Boom. Done!

> **_You write your own classes_**

## Yo 🫵 It's v0.5.4, W.I.P. Don't use it yet. Did tell you!

### STAY SANE! Low Code Verbosity. VERY 🐸 FIKO! [Demo Test here](https://fiko.rokma.rocks/)

🐸 GREAT STYLES WITH JUST ONE CSS FILE.
🐸 RESPONSIVE EVERYTHING.
🐸 VARIABLE EVERYTHING.
🐸 LIGHT OR DARK MODE.
🐸 USES NATIVE HTML.
🐸 LAYERS.
🐸 MODERN NORMALISE.
🐸 Low Code Verbosity.

# 🫵 USE IT

## Usage: **Install**

```shell
pnpm i fiko
```

## Usage: **Import**

```css
@import "node_modules/fiko/fiko.css";
```

then:

```html
<link rel="stylesheet" href="node_modules/fiko/package/fiko.css" />
```

Or

## Usage: **Download**

[Download FIKO](https://github.com/TOYBREAKER/fiko/fiko.zip) and link `/fiko.css` it in the `<head>` of your website.

```html
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

Most use case will need some custom, brand related styles...

## Usage: **CUSTOM CSS ON TOP OF FIKO**

Write your `my_custom_style.css` you can leverage the existing `fiko layers`, just mind the order`.

```css
/* ||| Layer Order Declaration ||| */
@layer base, root, toggle, containers, components;
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

## Use [Check colour contrast](https://colourcontrast.cc/) | [Devs here!](https://github.com/Pushedskydiver/Colour-Contrast-Checker)

.

# 🫵 DEVELOP

.

## FRONTEND [DEMO PAGE](https://fiko.rokma.rocks)

Fiko comes with a demo page, useful to test when dev.

Run a simple Python server on lh:3000. (Install Python for your sys first!)

```shell
# 🐲 DRY RECURRING START
echo '|';
echo 'cd package/';
cd dist/web/;
echo '|';
echo '🐲 now i am here:';
CWD=$(pwd -P)
echo $CWD
echo '|';
echo 'serve';
serve
```

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

.

## NPM CAVEAT

Sometimes you need to solve dep's issues. This helps a lot, many times:

```shell
pnpm install --install-strategy=nested`
```

`--install-strategy=nested`,
Formerly `legacy-bundling`,
instead of hoisting package installs in node_modules,
installs packages in the same manner that they are depended on.
NOTE: This may cause very deep directory structures and duplicate package installs as there is no de-duplicating.

.

# LIMITATIONS

FIKO can be used without custom CSS for quick or small projects. However, it’s designed to provide a starting point, like a “reset CSS on steroids”. Developing with `fiko.css` require modern CSS knowledge to add any custom look.

### BROWSER SUPPORT

FIKO is designed and tested for the latest stable Chrome, Firefox, Edge, and Safari releases. It does NOT support any version of IE, including IE 11.

### COPYRIGHT AND LICENSE

Licensed under the [MIT License](https://github.com/toybreaker/fiko/blob/master/LICENSE.md).

This slim starter was develop to scratch my own needs and it's inspired by today classless css framework such as [PICOCSS](https://github.com/picocss/pico),[WATER](https://github.com/kognise/water.css), [CSSBED](https://www.cssbed.com/), by [TOYBREAKER](https://github.com/toybreaker/)

.

# CHANGELOG

### v0.5.3

Nothing significant yet, just cleaner. Responsive padding setup.

### v0.5.0

Restart from ZERO.
Css Only. With variables, nesting, layers, dvh, dvw, oklch, etc..
2023 Platform. Let's Use it, Zod-damm-it!
New slim structure:

```
package/
  |- fiko.css
  |- index.html
```

### v0.4.1 DEAD END

Dont fix a broken house, It's faster to make a new one. Crucible moment. SCSS I love you but we gotta move on baby, there are new ways out there. New vehicle, fresh start.
