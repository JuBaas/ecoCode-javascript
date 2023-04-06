# Should not import all from library (`@ecocode/no-import-all-from-library`)

⚠️ This rule _warns_ in the ✅ `recommended` config.

<!-- end auto-generated rule header -->

## Rule details

This rule aims to reduce weight of programs by using only needed modules. Many libraries export only one module by
default, but some of them are exporting ES modules or submodules. We should use them to select more precisly needed
modules and avoid unnecessarily overloading files weight.

<!-- TODO: add bundle analyzer benchmarks -->

## Examples

Examples of **incorrect** code for this rule:

```js
// Example with lodash
import lodash from 'lodash';
import {isEmpty} from 'lodash';
import * as lodash from 'lodash';

// Example with underscore
import _ from 'underscore';
```

Examples of **correct** code for this rule:

```js
// Example with lodash (uses submodules)
import isEmpty from 'lodash/isEmpty';
import intersect from 'lodash/intersect';

// Example with underscore (uses esm modules)
import map from 'underscore/modules/map.js';
```