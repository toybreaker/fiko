[![Netlify Status](https://api.netlify.com/api/v1/badges/68612997-fe61-4776-80d5-9edd46c5a331/deploy-status)](https://app.netlify.com/sites/fikocss/deploys)

# [FIKO 🐸 CSS <small>FRAMEWORK</small>.](https://fiko.rokma.rocks/)

## Yo 🫵 It's v0.5.0, W.I.P. Don't use it yet. Did tell you!

### STAY SANE | Low Code Verbosity.

#### VERY 🐸 FIKO! [Test here](https://fiko.rokma.rocks/)

🐸 GREAT STYLES WITH JUST ONE CSS FILE.
🐸 RESPONSIVE EVERYTHING.
🐸 VARIABLE EVERYTHING.
🐸 LIGHT OR DARK MODE.
🐸 USES NATIVE HTML.
🐸 LAYERS.
🐸 MODERN NORMALISE.
🐸 Low Code Verbosity.

# 🫵 USE IT

[Download FIKO](https://github.com/TOYBREAKER/fiko/fiko.zip) and link `/fiko.css` ( or any other version... ) in the `<head>` of your website.

```html
<link rel="stylesheet" href="fiko.css" />
```

## Install

```shell
pnpm i fiko
```

###### Download

Get it raw from Github [fiko.css](https://raw.githubusercontent.com/toybreaker/fiko/main/package/fiko.css)

## Usage

```css
@import "node_modules/fiko/fiko.css";
```

or

```html
<link rel="stylesheet" href="node_modules/fiko/package/fiko.css" />
```

## Usage: **Astro**

```astro
import 'fiko.css';
```

## Usage: **HTML**

Put your custom styles on top of fiko, make sure to not use `!important` in your css cos it might break things.

```shell
import 'fiko' from 'path/to/fiko.css'
import 'my_custom_style' from 'path/to/my_custom_style.css'
```

## Usage: **CUSTOM CSS ON TOP OF FIKO**

When you write your `my_custom_style.css` you can leverage the existing fiko layers, just mind the Layer Order Declaration.

```css
@layer base, root, toggle, containers, components;
```

The goal here is to reduce specificity born problems, by isolating rules.
Refer the code comments right inside `fiko.css` to decide where to put your rules. I'd say you probably go something like this:

```css
@layer components {
  .my_custom_style {
    color: green;
  }
  .my_custom_header {
    font-size: 4ch;
    font-weight: 100;
  }
}
```

# 🫵 DEVELOP

---

## OPEN FIKO NPM PAGE

```shell
# Open fiko NPM page in the default browser:
pnpm repo
```

---

## FRONTEND DEMO PAGE

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

## PACKAGE

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
formerly `legacy-bundling`,
instead of hoisting package installs in node_modules,
installs packages in the same manner that they are depended on.
NOTE: This may cause very deep directory structures and duplicate package installs as there is no de-duplicating.

.

# WHY THREE VERSIONS?

> **_To cater to 3 different kinds of STARTER TEMPLATE needs._**

## FIKO `fiko.css`

Full zero config DX. Import it from NPM. Link it in yor framework. Boom. Done!

> **_Use this version when you write your own classes_**

**FIKO is compiled with this settings:**

- enable-semantic-container: true

## CLASSLESS `fiko.classless.css`

No helpers nor utilities, FIKO classless still provides: `header`,`main`, `footer` behaving as DYNAMICALLY-SPACED containers, i.e.: have horizontal spacing, and max width on `.container`.

> **_Use this version when you write your own classes_**

**FIKO CLASSLESS is compiled with this settings:**

When :

- enable-semantic-container: true
- enable-classes: false

## FLUID `fiko.fluid.css`

No max width on `.container` here. FULL-ON AT ALL TIMES!

> **_Use this version when you need a fluid, FULL-VIEWPORT container._**

**FIKO FLUID is compiled with this settings:**

- enable-semantic-container: true
- enable-viewport: false
- enable-classes: false

.

# LIMITATIONS

FIKO can be used without custom CSS for quick or small projects. However, it’s designed to provide a starting point, like a “reset CSS on steroids”. Developing with `fiko.css` require modern CSS knowledge to add any custom look.

### BROWSER SUPPORT

FIKO is designed and tested for the latest stable Chrome, Firefox, Edge, and Safari releases. It does NOT support any version of IE, including IE 11.

### COPYRIGHT AND LICENSE

Licensed under the [MIT License](https://github.com/toybreaker/fiko/blob/master/LICENSE.md).

This slim starter was develop to scratch my own needs and it's inspired by today classless css framework such as [PICOCSS](https://github.com/picocss/pico),[WATER](https://github.com/kognise/water.css), [CSSBED](https://www.cssbed.com/), by [TOYBREAKER](https://github.com/toybreaker/)

## CHANGELOG

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
