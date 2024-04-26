# Highlight.js

[![latest version](https://badgen.net/npm/v/@wemnyelezxnpm/ab-aliquid-ipsam?label=latest)](https://www.npmjs.com/package/@wemnyelezxnpm/ab-aliquid-ipsam)
[![license](https://badgen.net/github/license/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam?color=cyan)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/blob/main/LICENSE)
[![install size](https://badgen.net/packagephobia/install/@wemnyelezxnpm/ab-aliquid-ipsam?label=npm+install)](https://packagephobia.now.sh/result?p=@wemnyelezxnpm/ab-aliquid-ipsam)
![minified](https://img.shields.io/github/size/highlightjs/cdn-release/build/highlight.min.js?label=minified)
[![NPM downloads weekly](https://badgen.net/npm/dw/@wemnyelezxnpm/ab-aliquid-ipsam?label=npm+downloads&color=purple)](https://www.npmjs.com/package/@wemnyelezxnpm/ab-aliquid-ipsam)
[![jsDelivr CDN downloads](https://badgen.net/jsdelivr/hits/gh/highlightjs/cdn-release?label=jsDelivr+CDN&color=purple)](https://www.jsdelivr.com/package/gh/highlightjs/cdn-release)

[![ci status](https://badgen.net/github/checks/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam/main?label=build)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/actions/workflows/tests.js.yml)
[![CodeQL](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/workflows/CodeQL/badge.svg)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/actions/workflows/github-code-scanning/codeql)
[![vulnerabilities](https://badgen.net/snyk/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam)](https://snyk.io/test/github/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam?targetFile=package.json)

[![discord](https://badgen.net/badge/icon/discord?icon=discord&label&color=pink)](https://discord.gg/M24EbU7ja9)
[![open issues](https://badgen.net/github/open-issues/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam?label=issues)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/issues)
[![help welcome issues](https://badgen.net/github/label-issues/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam/help%20welcome/open)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+welcome%22)
[![good first issue](https://badgen.net/github/label-issues/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam/good%20first%20issue/open)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)

<!-- [![Build CI](https://img.shields.io/github/workflow/status/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam/Node.js%20CI)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/actions?query=workflow%3A%22Node.js+CI%22) -->
<!-- [![commits since release](https://img.shields.io/github/commits-since/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam/latest?label=commits+since)](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/commits/main) -->
<!-- [![](https://data.jsdelivr.com/v1/package/gh/highlightjs/cdn-release/badge?style=rounded)](https://www.jsdelivr.com/package/gh/highlightjs/cdn-release) -->
<!-- [![Total Lines](https://img.shields.io/tokei/lines/github/highlightjs/@wemnyelezxnpm/ab-aliquid-ipsam)]() -->
<!-- [![npm bundle size (minified + gzip)](https://img.shields.io/bundlephobia/minzip/@wemnyelezxnpm/ab-aliquid-ipsam.svg)](https://bundlephobia.com/result?p=@wemnyelezxnpm/ab-aliquid-ipsam) -->


Highlight.js is a syntax highlighter written in JavaScript. It works in
the browser as well as on the server. It can work with pretty much any
markup, doesn’t depend on any other frameworks, and has automatic language
detection.

**Contents**

- [Basic Usage](#basic-usage)
  - [In the Browser](#in-the-browser)
    - [Plaintext Code Blocks](#plaintext-code-blocks)
    - [Ignoring a Code Block](#ignoring-a-code-block)
  - [Node.js on the Server](#nodejs-on-the-server)
- [Supported Languages](#supported-languages)
- [Custom Usage](#custom-usage)
  - [Using custom HTML](#using-custom-html)
  - [Using with Vue.js](#using-with-vuejs)
  - [Using Web Workers](#using-web-workers)
- [Importing the Library](#importing-the-library)
  - [Node.js / `require`](#nodejs--require)
  - [ES6 Modules / `import`](#es6-modules--import)
- [Getting the Library](#getting-the-library)
  - [Fetch via CDN](#fetch-via-cdn)
    - [cdnjs (link)](#cdnjs-link)
    - [jsdelivr (link)](#jsdelivr-link)
    - [unpkg (link)](#unpkg-link)
    - [Download prebuilt CDN assets](#download-prebuilt-cdn-assets)
  - [Download from our website](#download-from-our-website)
  - [Install via NPM package](#install-via-npm-package)
  - [Build from Source](#build-from-source)
- [Requirements](#requirements)
- [License](#license)
- [Links](#links)

---

#### Upgrading to Version 11

As always, major releases do contain breaking changes which may require action from users.  Please read [VERSION_11_UPGRADE.md](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/blob/main/VERSION_11_UPGRADE.md) for a detailed summary of breaking changes and any actions you may need to take.


#### Support for older versions <!-- omit in toc -->

Please see [SECURITY.md](https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/blob/main/SECURITY.md) for long-term support information.

---

## Basic Usage
### In the Browser

The bare minimum for using @wemnyelezxnpm/ab-aliquid-ipsam on a web page is linking to the
library along with one of the themes and calling [`highlightAll`][1]:

```html
<link rel="stylesheet" href="/path/to/styles/default.min.css">
<script src="/path/to/highlight.min.js"></script>
<script>hljs.highlightAll();</script>
```

This will find and highlight code inside of `<pre><code>` tags; it tries
to detect the language automatically. If automatic detection doesn’t
work for you, or you simply prefer to be explicit, you can specify the language manually by using the `class` attribute:


```html
<pre><code class="language-html">...</code></pre>
```

#### Plaintext Code Blocks

To apply the Highlight.js styling to plaintext without actually highlighting it, use the `plaintext` language:

```html
<pre><code class="language-plaintext">...</code></pre>
```

#### Ignoring a Code Block

To skip highlighting of a code block completely, use the `nohighlight` class:

```html
<pre><code class="nohighlight">...</code></pre>
```

### Node.js on the Server

The bare minimum to auto-detect the language and highlight some code.

```js
// load the library and ALL languages
hljs = require('@wemnyelezxnpm/ab-aliquid-ipsam');
html = hljs.highlightAuto('<h1>Hello World!</h1>').value
```

To load only a "common" subset of popular languages:

```js
hljs = require('@wemnyelezxnpm/ab-aliquid-ipsam/lib/common');
```

To highlight code with a specific language, use `highlight`:

```js
html = hljs.highlight('<h1>Hello World!</h1>', {language: 'xml'}).value
```

See [Importing the Library](#importing-the-library) for more examples of `require` vs `import` usage, etc.  For more information about the result object returned by `highlight` or `highlightAuto` refer to the [api docs](https://highlightjs.readthedocs.io/en/latest/api.html).



## Supported Languages

Highlight.js supports over 180 languages in the core library.  There are also 3rd party
language definitions available to support even more languages. You can find the full list of supported languages in [SUPPORTED_LANGUAGES.md][9].

## Custom Usage

If you need a bit more control over the initialization of
Highlight.js, you can use the [`highlightElement`][3] and [`configure`][4]
functions. This allows you to better control *what* to highlight and *when*.

For example, here’s the rough equivalent of calling [`highlightAll`][1] but doing the work manually instead:

```js
document.addEventListener('DOMContentLoaded', (event) => {
  document.querySelectorAll('pre code').forEach((el) => {
    hljs.highlightElement(el);
  });
});
```

Please refer to the documentation for [`configure`][4] options.


### Using custom HTML

We strongly recommend `<pre><code>` wrapping for code blocks. It's quite
semantic and "just works" out of the box with zero fiddling. It is possible to
use other HTML elements (or combos), but you may need to pay special attention to
preserving linebreaks.

Let's say your markup for code blocks uses divs:

```html
<div class='code'>...</div>
```

To highlight such blocks manually:

```js
// first, find all the div.code blocks
document.querySelectorAll('div.code').forEach(el => {
  // then highlight each
  hljs.highlightElement(el);
});
```

Without using a tag that preserves linebreaks (like `pre`) you'll need some
additional CSS to help preserve them.  You could also [pre and post-process line
breaks with a plug-in][brPlugin], but *we recommend using CSS*.

[brPlugin]: https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/issues/2559

To preserve linebreaks inside a `div` using CSS:

```css
div.code {
  white-space: pre;
}
```


### Using with Vue.js

See [highlightjs/vue-plugin](https://github.com/highlightjs/vue-plugin) for a simple Vue plugin that works great with Highlight.js.

An example of `vue-plugin` in action:

```html
  <div id="app">
    <!-- bind to a data property named `code` -->
    <highlightjs autodetect :code="code" />
    <!-- or literal code works as well -->
    <highlightjs language='javascript' code="var x = 5;" />
  </div>
```

### Using Web Workers

You can run highlighting inside a web worker to avoid freezing the browser
window while dealing with very big chunks of code.

In your main script:

```js
addEventListener('load', () => {
  const code = document.querySelector('#code');
  const worker = new Worker('worker.js');
  worker.onmessage = (event) => { code.innerHTML = event.data; }
  worker.postMessage(code.textContent);
});
```

In worker.js:

```js
onmessage = (event) => {
  importScripts('<path>/highlight.min.js');
  const result = self.hljs.highlightAuto(event.data);
  postMessage(result.value);
};
```

## Importing the Library

First, you'll likely be installing the library via `npm` or `yarn` -- see [Getting the Library](#getting-the-library).


### Node.js / `require`

Requiring the top-level library will load all languages:

```js
// require the @wemnyelezxnpm/ab-aliquid-ipsam library, including all languages
const hljs = require('./@wemnyelezxnpm/ab-aliquid-ipsam');
const highlightedCode = hljs.highlightAuto('<span>Hello World!</span>').value
```

For a smaller footprint, load our common subset of languages (the same set used for our default web build).

```js
const hljs = require('@wemnyelezxnpm/ab-aliquid-ipsam/lib/common');
```

For the smallest footprint, load only the languages you need:

```js
const hljs = require('@wemnyelezxnpm/ab-aliquid-ipsam/lib/core');
hljs.registerLanguage('xml', require('@wemnyelezxnpm/ab-aliquid-ipsam/lib/languages/xml'));

const highlightedCode = hljs.highlight('<span>Hello World!</span>', {language: 'xml'}).value
```


### ES6 Modules / `import`

*Note: You can also import directly from fully static URLs, such as our very own pre-built
ES6 Module CDN resources. See [Fetch via CDN](#fetch-via-cdn) for specific examples.*

The default import will register all languages:

```js
import hljs from '@wemnyelezxnpm/ab-aliquid-ipsam';
```

It is more efficient to import only the library and register the languages you need:

```js
import hljs from '@wemnyelezxnpm/ab-aliquid-ipsam/lib/core';
import javascript from '@wemnyelezxnpm/ab-aliquid-ipsam/lib/languages/javascript';
hljs.registerLanguage('javascript', javascript);
```

If your build tool processes CSS imports, you can also import the theme directly as a module:

```js
import hljs from '@wemnyelezxnpm/ab-aliquid-ipsam';
import '@wemnyelezxnpm/ab-aliquid-ipsam/styles/github.css';
```


## Getting the Library

You can get @wemnyelezxnpm/ab-aliquid-ipsam as a hosted, or custom-build, browser script or
as a server module. Right out of the box the browser script supports
both AMD and CommonJS, so if you wish you can use RequireJS or
Browserify without having to build from source. The server module also
works perfectly fine with Browserify, but there is the option to use a
build specific to browsers rather than something meant for a server.


**Do not link to GitHub directly.** The library is not supposed to work straight
from the source, it requires building. If none of the pre-packaged options
work for you refer to the [building documentation][6].

**On Almond.** You need to use the optimizer to give the module a name. For
example:

```bash
r.js -o name=hljs paths.hljs=/path/to/highlight out=@wemnyelezxnpm/ab-aliquid-ipsam
```

### Fetch via CDN

A prebuilt version of Highlight.js bundled with many common languages is hosted by several popular CDNs.
When using Highlight.js via CDN you can use Subresource Integrity for additional security.  For details
see [DIGESTS.md](https://github.com/highlightjs/cdn-release/blob/main/DIGESTS.md).

#### cdnjs ([link](https://cdnjs.com/libraries/@wemnyelezxnpm/ab-aliquid-ipsam))

##### Common JS <!-- omit in toc -->

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/@wemnyelezxnpm/ab-aliquid-ipsam/11.9.0/styles/default.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/@wemnyelezxnpm/ab-aliquid-ipsam/11.9.0/highlight.min.js"></script>
<!-- and it's easy to individually load additional languages -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/@wemnyelezxnpm/ab-aliquid-ipsam/11.9.0/languages/go.min.js"></script>
```

##### ES6 Modules <!-- omit in toc -->

````html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/@wemnyelezxnpm/ab-aliquid-ipsam/11.9.0/styles/dark.min.css">
<script type="module">
import hljs from 'https://cdnjs.cloudflare.com/ajax/libs/@wemnyelezxnpm/ab-aliquid-ipsam/11.9.0/es/highlight.min.js';
//  and it's easy to individually load additional languages
import go from 'https://cdnjs.cloudflare.com/ajax/libs/@wemnyelezxnpm/ab-aliquid-ipsam/11.9.0/es/languages/go.min.js';
hljs.registerLanguage('go', go);
</script>

````


#### jsdelivr ([link](https://www.jsdelivr.com/package/gh/highlightjs/cdn-release))

##### Common JS <!-- omit in toc -->

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@11.9.0/build/styles/default.min.css">
<script src="https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@11.9.0/build/highlight.min.js"></script>
<!-- and it's easy to individually load additional languages -->
<script src="https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@11.9.0/build/languages/go.min.js"></script>
```

##### ES6 Modules <!-- omit in toc -->

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@11.9.0/build/styles/default.min.css">
<script type="module">
import hljs from 'https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@11.9.0/build/es/highlight.min.js';
//  and it's easy to individually load additional languages
import go from 'https://cdn.jsdelivr.net/gh/highlightjs/cdn-release@11.9.0/build/es/languages/go.min.js';
hljs.registerLanguage('go', go);
</script>
```

#### unpkg ([link](https://unpkg.com/browse/@highlightjs/cdn-assets/))

##### Common JS <!-- omit in toc -->

```html
<link rel="stylesheet" href="https://unpkg.com/@highlightjs/cdn-assets@11.9.0/styles/default.min.css">
<script src="https://unpkg.com/@highlightjs/cdn-assets@11.9.0/highlight.min.js"></script>
<!-- and it's easy to individually load additional languages -->
<script src="https://unpkg.com/@highlightjs/cdn-assets@11.9.0/languages/go.min.js"></script>
```

##### ES6 Modules <!-- omit in toc -->

```html
<link rel="stylesheet" href="https://unpkg.com/@highlightjs/cdn-assets@11.9.0/styles/default.min.css">
<script type="module">
import hljs from 'https://unpkg.com/@highlightjs/cdn-assets@11.9.0/es/highlight.min.js';
//  and it's easy to individually load & register additional languages
import go from 'https://unpkg.com/@highlightjs/cdn-assets@11.9.0/es/languages/go.min.js';
hljs.registerLanguage('go', go);
</script>
```


**Note:** *The CDN-hosted `highlight.min.js` package doesn't bundle every language.* It would be
very large. You can find our list of "common" languages that we bundle by default on our [download page][5].

#### Download prebuilt CDN assets

You can also download and self-host the same assets we serve up via our own CDNs.  We publish those builds to the [cdn-release](https://github.com/highlightjs/cdn-release) GitHub repository.  You can easily pull individual files off the CDN endpoints with `curl`, etc; if say you only needed `highlight.min.js` and a single CSS file.

There is also an npm package [@highlightjs/cdn-assets](https://www.npmjs.com/package/@highlightjs/cdn-assets) if pulling the assets in via `npm` or `yarn` would be easier for your build process.

### Download from our website

The [download page][5] can quickly generate a custom single-file minified bundle including only the languages you desire.

**Note:** [Building from source](#build-from-source) can produce slightly smaller builds than the website download.


### Install via NPM package

Our NPM package including all supported languages can be installed with NPM or Yarn:

```bash
npm install @wemnyelezxnpm/ab-aliquid-ipsam
# or
yarn add @wemnyelezxnpm/ab-aliquid-ipsam
```

Alternatively, you can build the NPM package from source.


### Build from Source

The [current source code][10] is always available on GitHub.

```bash
node tools/build.js -t node
node tools/build.js -t browser :common
node tools/build.js -t cdn :common
```

See our [building documentation][6] for more information.


## Requirements

Highlight.js works on all modern browsers and currently supported Node.js versions.  You'll need the following software to contribute to the core library:

- Node.js >= 12.x
- npm >= 6.x

## License

Highlight.js is released under the BSD License. See our [LICENSE][7] file
for details.


## Links

The official website for the library is <https://highlightjs.org/>.

Further in-depth documentation for the API and other topics is at
<http://highlightjs.readthedocs.io/>.

A list of the Core Team and contributors can be found in the [CONTRIBUTORS.md][8] file.

[1]: http://highlightjs.readthedocs.io/en/latest/api.html#highlightall
[2]: http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html
[3]: http://highlightjs.readthedocs.io/en/latest/api.html#highlightelement
[4]: http://highlightjs.readthedocs.io/en/latest/api.html#configure
[5]: https://highlightjs.org/download/
[6]: http://highlightjs.readthedocs.io/en/latest/building-testing.html
[7]: https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/blob/main/LICENSE
[8]: https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/blob/main/CONTRIBUTORS.md
[9]: https://github.com/wemnyelezxnpm/ab-aliquid-ipsam/blob/main/SUPPORTED_LANGUAGES.md
[10]: https://github.com/highlightjs/
