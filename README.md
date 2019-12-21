1. Run `yarn`
2. Run  `yarn ngcc --create-ivy-entry-points`
3. Inspect `node_modules/@angular/core/__ivy_ngcc__/bundles/core.umd.js`

Notice how there are multiple trailing commas in expressions that cause
syntax errors in IE11.

```js
typeof exports === 'object' && typeof module !== 'undefined' ? factory(exports, require('rxjs'), require('rxjs/operators'),) :
```