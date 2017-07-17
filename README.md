Vanrose
------

> Van Helsing used to put Wild Roses on coffins to immobilize vampires. Now, the times have changed. Put Vanrose on hunted docs objects, to empower them.

Supplementary tool for [Vandoc](https://github.com/ArmorDarks/Vandoc).

* Accepts Vandoc result object
* Provides handy methods to work with object

_So far it is only initial draft._

#### Methods

```js
const v = vanrose(vandocData, { cwd: '/source' })
```

* `v.cwd()` — returns current working directory
* `v.filterLanguage('languageName')` — returns entries only for specified language.
* `v.toc()` — returns Object with Table of Content based on inner values with appropriate links for each entry, taking into account `cwd`.
* `v.href(':module/path')` — creates proper `href` from `Namepath` which can be used for anchors.
* `v.module('myModule/path')` — returns associated with specified module entries
* `v.rejectPrivate()` — filters out entries with `private: true`
* `v.rejectIgnored()` — filters out entries with `ignored: true`
* `v.entry('namepath')` — returns entry
* `v.entry('namepath').signature()` — returns entry signature (if there are any) with all params and Flow-style type annotation: `input: number, name?: string`

   This function can be extended later to return signature with different annotation styles.