# astro

## 0.13.11

### Patch Changes

- 6573bea: Fixed README header aspect ratio

## 0.13.10

### Patch Changes

- 233fbcd: Fix race condition caused by parallel build
- Updated dependencies [7f8d586]
  - @astrojs/parser@0.13.10

## 0.13.9

### Patch Changes

- 3ada25d: Pass configured Tailwind config file to the tailwindcss plugin
- f9f2da4: Add repository key to all package.json
- Updated dependencies [f9f2da4]
  - @astrojs/parser@0.13.9
  - @astrojs/prism@0.2.2
  - @astrojs/markdown-support@0.1.2

## 0.13.8

### Patch Changes

- 251b0b5: Less verbose HMR script
- 54c291e: Fix <script type="module"> resolution
- 272769d: Improve asset resolution
- 490f2be: Add support for Fragments with `<>` and `</>` syntax
- Updated dependencies [490f2be]
  - @astrojs/parser@0.13.8

## 0.13.7

### Patch Changes

- Updated dependencies [9d4a40f]
  - @astrojs/renderer-preact@0.1.2
  - @astrojs/renderer-react@0.1.2

## 0.13.6

### Patch Changes

- 016833a: Honors users HMR settings
- 73a43d9: Prevent dev from locking up on empty selectors

## 0.13.5

### Patch Changes

- 9f51e2d: Fix issue with arrow components in Preact/React

## 0.13.4

### Patch Changes

- 2d85409: Fixes serialization of boolean attributes
- e0989c6: Fix scoped CSS selector when class contains a colon
- 42dee79: Allows doctype to be written with any casing

## 0.13.3

### Patch Changes

- ab2972b: Update package.json engines for esm support
- Updated dependencies [ab2972b]
  - @astrojs/parser@0.13.3
  - @astrojs/prism@0.2.1
  - @astrojs/renderer-preact@0.1.1
  - @astrojs/renderer-react@0.1.1
  - @astrojs/renderer-svelte@0.1.1
  - @astrojs/renderer-vue@0.1.2

## 0.13.2

### Patch Changes

- c374a54: Bugfix: createCollection() API can be used without fetchContent()

## 0.13.1

### Patch Changes

- 61b5590: Pass "site" config to Snowpack as "baseUrl"

## 0.13.0

### Minor Changes

- ce93361: Set the minimum Node version in the engines field
- 1bab906: Removes a second instance of snowpack which degraded peformance

### Patch Changes

- 5fbc1cb: nit: ask user to modify devOptions.port when addr in use for dev

## 0.12.10

### Patch Changes

- 5cda571: Fix an issue with how files are watched during development

## 0.12.9

### Patch Changes

- 21b0c73: Removes some warnings that are internal to Astro

## 0.12.8

### Patch Changes

- f66fd1f: Fixes regression caused by attempting to prebuild an internal dep

## 0.12.7

### Patch Changes

- f6ef53b: Fixed a bug where recursive markdown was not working properly
- 5a871f3: Fixes logging to default to the info level
- f4a747f: improve build output

## 0.12.6

### Patch Changes

- 522c873: Fixes bug where astro build would fail when trying to log

## 0.12.5

### Patch Changes

- b1364af: Updates logging to display messages from Snowpack
- cc532cd: Properly resolve `tailwindcss` depedency if using Tailwind
- Updated dependencies [b1364af]
  - @astrojs/renderer-vue@0.1.1

## 0.12.4

### Patch Changes

- 0d6afae: Fixes a few small bugs with the `Markdown` component when there are multiple instances on the same page
- 1d930ff: Adds [`--verbose`](https://github.com/snowpackjs/astro/blob/main/docs/cli.md#--verbose) and [`--reload`](https://github.com/snowpackjs/astro/blob/main/docs/cli.md#--reload) flags to the `astro` CLI.

## 0.12.3

### Patch Changes

- fe6a985: Fixes resolution when esinstall installs Markdown and Prism components

## 0.12.2

### Patch Changes

- 50e6f49: Fixes issues with using astro via the create script
- Updated dependencies [50e6f49]
  - @astrojs/markdown-support@0.1.1

## 0.12.1

### Patch Changes

- Updated dependencies [6de740d]
  - astro-parser@0.12.1

## 0.12.0

### Minor Changes

- 8ff7998: Enable Snowpack's [built-in HMR support](https://www.snowpack.dev/concepts/hot-module-replacement) to enable seamless live updates while editing.
- ffb6380: Support for dynamic Markdown through the content attribute.
- 8ff7998: Enabled Snowpack's built-in HMR engine for Astro pages
- 643c880: **This is a breaking change**

  Updated the rendering pipeline for `astro` to truly support any framework.

  For the vast majority of use cases, `astro` should _just work_ out of the box. Astro now depends on `@astrojs/renderer-preact`, `@astrojs/renderer-react`, `@astrojs/renderer-svelte`, and `@astrojs/renderer-vue`, rather than these being built into the core library. This opens the door for anyone to contribute additional renderers for Astro to support their favorite framework, as well as the ability for users to control which renderers should be used.

  **Features**

  - Expose a pluggable interface for controlling server-side rendering and client-side hydration
  - Allows components from different frameworks to be nested within each other.
    > Note: `svelte` currently does support non-destructive hydration, so components from other frameworks cannot currently be nested inside of a Svelte component. See https://github.com/sveltejs/svelte/issues/4308.

  **Breaking Changes**

  - To improve compiler performance, improve framework support, and minimize JS payloads, any children passed to hydrated components are automatically wrapped with an `<astro-fragment>` element.

### Patch Changes

- 3d20623: Fixed a bug where Astro did not conform to JSX Expressions' [`&&`](https://reactjs.org/docs/conditional-rendering.html#inline-if-with-logical--operator) syntax.

  Also fixed a bug where `<span data-attr="" />` would render as `<span data-attr="undefined" />`.

- 46871d2: Fixed bug where a class attribute was added to the doctype
- c9d833e: Fixed a number of bugs and re-enabled the `@astrojs/renderer-vue` renderer
- ce30bb0: Temporarily disable `@astrojs/renderer-vue` while we investigate an issue with installation
- addd67d: Rename `astroConfig` to `pages` in config. Docs updated.
- d2330a5: Improve error display for missing local files
- Updated dependencies [643c880]
- Updated dependencies [d2330a5]
- Updated dependencies [c9d833e]
  - @astrojs/renderer-preact@0.1.0
  - @astrojs/renderer-react@0.1.0
  - @astrojs/renderer-svelte@0.1.0
  - @astrojs/renderer-vue@0.1.0
  - astro-parser@0.12.0

## 0.12.0-next.1

### Patch Changes

- ce30bb0: Temporarily disable `@astrojs/renderer-vue` while we investigate an issue with installation

## 0.12.0-next.0

### Minor Changes

- 8ff7998: Enable Snowpack's [built-in HMR support](https://www.snowpack.dev/concepts/hot-module-replacement) to enable seamless live updates while editing.
- 8ff7998: Enabled Snowpack's built-in HMR engine for Astro pages
- 643c880: **This is a breaking change**

  Updated the rendering pipeline for `astro` to truly support any framework.

  For the vast majority of use cases, `astro` should _just work_ out of the box. Astro now depends on `@astrojs/renderer-preact`, `@astrojs/renderer-react`, `@astrojs/renderer-svelte`, and `@astrojs/renderer-vue`, rather than these being built into the core library. This opens the door for anyone to contribute additional renderers for Astro to support their favorite framework, as well as the ability for users to control which renderers should be used.

  **Features**

  - Expose a pluggable interface for controlling server-side rendering and client-side hydration
  - Allows components from different frameworks to be nested within each other.
    > Note: `svelte` currently does support non-destructive hydration, so components from other frameworks cannot currently be nested inside of a Svelte component. See https://github.com/sveltejs/svelte/issues/4308.

  **Breaking Changes**

  - To improve compiler performance, improve framework support, and minimize JS payloads, any children passed to hydrated components are automatically wrapped with an `<astro-fragment>` element.

### Patch Changes

- 3d20623: Fixed a bug where Astro did not conform to JSX Expressions' [`&&`](https://reactjs.org/docs/conditional-rendering.html#inline-if-with-logical--operator) syntax.

  Also fixed a bug where `<span data-attr="" />` would render as `<span data-attr="undefined" />`.

- Updated dependencies [643c880]
  - @astrojs/renderer-preact@0.1.0-next.0
  - @astrojs/renderer-react@0.1.0-next.0
  - @astrojs/renderer-svelte@0.1.0-next.0
  - @astrojs/renderer-vue@0.1.0-next.0

## 0.11.0

### Minor Changes

- 19e20f2: Add Tailwind JIT support for Astro

### Patch Changes

- c43ee95: Bugfix: CSS bundling randomizes order
- 9cdada0: Fixes a few edge case bugs with Astro's handling of Markdown content
- Updated dependencies [9cdada0]
  - astro-parser@0.11.0

## 0.10.0

`astro` has been bumped to `0.10.0` to avoid conflicts with the previously published `astro` package (which was graciously donated to us at `v0.9.2`).

### Minor Changes

- b3886c2: Enhanced **Markdown** support! Markdown processing has been moved from `micromark` to `remark` to prepare Astro for user-provided `remark` plugins _in the future_.

  This change also introduces a built-in `<Markdown>` component for embedding Markdown and any Astro-supported component format inside of `.astro` files. [Read more about Astro's Markdown support.](https://github.com/snowpackjs/astro/blob/main/docs/markdown.md)

### Patch Changes

- 9d092b5: Bugfix: Windows collection API path bug
- Updated dependencies [b3886c2]
  - astro-parser@0.1.0

## 0.0.13

### Patch Changes

- 7184149: Added canonical URL and site globals for .astro files
- b81abd5: Add CSS bundling
- 7b55d3d: chore: Remove non-null assertions
- 000464b: Fix bug when building Svelte components
- 95b1733: Fix: wait for async operation to finish
- e0a4f5f: Allow renaming for default import components
- 9feffda: Bugfix: fixes double <pre> tags generated from markdown code blocks
- 87ab4c6: Bugfix: Scoped CSS with pseudoclasses and direct children selectors
- e0fc2ca: fix: build stuck on unhandled promise reject

## 0.0.11

### Patch Changes

- 3ad0aac: Fix `fetchContent` API bug for nested `.md` files

## 0.0.10

### Patch Changes

- d924fcb: Fix issue with Prism component missing dependency
- Updated dependencies [d924fcb]
  - astro-prism@0.0.2
