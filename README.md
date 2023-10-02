[![Netlify Status](https://api.netlify.com/api/v1/badges/68612997-fe61-4776-80d5-9edd46c5a331/deploy-status)](https://app.netlify.com/sites/fikocss/deploys)

# [FIKO 🐸 CSS <small>FRAMEWORK</small>.](https://fiko.rokma.rocks/)

### STAY SANE! LOW CODE VERBOSITY, just few classes with `var(--magic)`, VERY FIKO!

> **"YO, THIS IN FULL-ON WORK IN PROGRESS. I'm telling 🫵 you!"**

VERSION: 0.2.11

TEST: [FIKO 🐸 CSS test](https://fiko.rokma.rocks/test/)

- 🐸 GREAT STYLES WITH JUST ONE CSS FILE
- 🐸 RESPONSIVE EVERYTHING
- 🐸 LIGHT OR DARK MODE
- 🐸 USES THE SEMANTICS OF NATIVE HTML TAGS.
- 🐸 CLASSLESS OPTION.
- 🐸 FULL `fiko.min.css` version. 11 CLASSES. 26kb.
- 🐸 CLASSLESS `fiko.classless.min.css`. ZERO CLASSES. 24kB.
- 🐸 FLUID `fiko.fluid.classless.min.css` FULL-VIEWPORT, ZERO CLASSES versions. 24kB.

# 🫵 USE IT

[Download FIKO](https://github.com/TOYBREAKER/fiko/fiko.zip) and link `/css/fiko.min.css` ( or any other version... ) in the `<head>` of your website.

```html
<link rel="stylesheet" href="css/fiko.min.css" />
```

### Install with pnpm (or npm)

```shell
pnpm i fiko
```

---

## Usage: **Astro**

```astro
import 'alku/alku.css';
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
echo 'cd src/web/';
cd src/web/;
echo '|';
echo '🐲 now i am here:';
CWD=$(pwd -P)
echo $CWD
echo '|';
echo 'cd serve';
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
pnpm create astro@latest && pnpm astro add fiko
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

# WHY THREE VERSIONS?

> **_To cater to 3 different kinds of STARTER TEMPLATE needs._**

## CLASSLESS

`fiko.classless.css`
No helpers nor utilities, FIKO classless still provides: `header`,`main`, `footer` behaving as DYNAMICALLY-SPACED containers, i.e.: have horizontal spacing, and max width on `.container`.

> **_Use this version if you need centred viewports_**

## FLUID

Or use the `fiko.fluid.classless.css` version.
When you need a fluid, FULL-VIEWPORT container. No max width on `.container` here. FULL-ON AT ALL TIMES!

# LIMITATIONS

FIKO can be used without custom CSS for quick or small projects. However, it’s designed to provide a starting point, like a “reset CSS on steroids”. Developing with `fiko.css` require modern CSS knowledge to add any custom look.

### BROWSER SUPPORT

FIKO is designed and tested for the latest stable Chrome, Firefox, Edge, and Safari releases. It does NOT support any version of IE, including IE 11.

### COPYRIGHT AND LICENSE

Licensed under the [MIT License](https://github.com/toybreaker/fiko/blob/master/LICENSE.md).

THIS SLIM STARTER WAS DEVELOP TO SCRATCH MY OWN NEEDS AND IT'S INSPIRED BY TODAY CLASSLESS CSS FRAMEWORK SUCH AS [PICOCSS](https://github.com/picocss/pico),[WATER](https://github.com/kognise/water.css), [CSSBED](https://www.cssbed.com/), BY [TOYBREAKER](https://github.com/toybreaker/)

```

```
