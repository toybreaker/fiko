[![Netlify Status](https://api.netlify.com/api/v1/badges/68612997-fe61-4776-80d5-9edd46c5a331/deploy-status)](https://app.netlify.com/sites/fikocss/deploys)

# [FIKO 🐸 CSS <small>FRAMEWORK</small>.](https://fiko.rokma.rocks/)

## YO 🫵 IT'S ONLY VERSION 0.3.10, IT'S W.I.P.

## DON'T 🫵 USE IT YET! Did tell you!

### STAY SANE | Low Code Verbosity, just few Classes with `var(--magic)`

#### VERY 🐸 FIKO! [Test here](https://fiko.rokma.rocks/)

- 🐸 GREAT STYLES WITH JUST ONE CSS FILE
- 🐸 RESPONSIVE EVERYTHING
- 🐸 LIGHT OR DARK MODE
- 🐸 USES THE SEMANTICS OF NATIVE HTML TAGS.
- 🐸 CLASSLESS OPTION.
- 🐸 FULL `fiko.css` version. 11 CLASSES. 26kb.
- 🐸 CLASSLESS `fiko.classless.css`. ZERO CLASSES. 24kB.
- 🐸 FLUID `fiko.fluid.classless.css` FULL-VIEWPORT, ZERO CLASSES. 24kB.

# 🫵 USE IT

[Download FIKO](https://github.com/TOYBREAKER/fiko/fiko.zip) and link `/fiko.css` ( or any other version... ) in the `<head>` of your website.

```html
<link rel="stylesheet" href="fiko.css" />
```

### Install with pnpm (or npm)

```shell
pnpm i fiko
```

---

## Usage: **Astro**

```astro
import 'fiko.css';
```

## Usage: **HTML**

```shell
import 'fiko' from 'path/to/fiko.css'
import 'my_custom_style' from 'path/to/my_custom_style.css'
```

---

# 🫵 DEVELOP CLI STUFF

---

## FRONTEND

Run a simple Python server on lh:3000.
(You'll need to install Python for your sys first!)

```shell
# 🐲 DRY RECURRING START
echo '|';
echo 'cd dist/web/';
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

## BUILD

```shell
# BUILD.
pnpm run F
```

## DEV

```shell
# DEV:
pnpm run dev
```

or with bash shortcut:

```shell
prc
```

## LINT

```shell
# LINT:
pnpm run lint
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

## OPEN FIKO NPM PAGE

```shell
# Open fiko NPM page in the default browser:
pnpm repo
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

THIS SLIM STARTER WAS DEVELOP TO SCRATCH MY OWN NEEDS AND IT'S INSPIRED BY TODAY CLASSLESS CSS FRAMEWORK SUCH AS [PICOCSS](https://github.com/picocss/pico),[WATER](https://github.com/kognise/water.css), [CSSBED](https://www.cssbed.com/), BY [TOYBREAKER](https://github.com/toybreaker/)

## CHANGELOG

### v0.5.0 CSS2023

Restart from ZERO. Css Only. 2023 Platform. Use it, Zod-dam-it!
Find all in `src/css2024`` folder.

### v0.4.1 DEAD END

TLDR Too Long Don't Read.
WHAT IT MEANS TO FAIL QUICK AND MANY TIMES.
Dont fix a broken house, make a new from zero. Faster.
While loving and still using Piko, this FIKO project has a new goal a new 2023 platform to use, and is better solved with a fresh start.
SCSS i love but i gotta move on baby, there are new ways out there.
CSS 2023 with layers, container queries, nesting, subgrid is all new fun now.
Been here since the start of it YOL
Faster, Cleaner, Leaner Better.
CSS2023

### v0.5.0

new structure:

```
css/
  |- layers/
  |  |- layer0.css
  |  |- layer1.css
  |  |- layer2.css
  |  |- layer3.css
  |- root.css
  |- reset.css
  |- light-dark-toggle.css
  |- main.css
  |- index.html
```
