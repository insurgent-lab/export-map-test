# @skypack/export-map-test

Package that illustrates different ways to expose entry points via `package.json`’s `"exports"` field ([see Node.js docs](https://nodejs.org/api/packages.html#packages_package_entry_points)).

```
npm i @skypack/export-map-test
```

### Conditions:

- ✅ `@skypack/export-map-test` (main entry): should import `./module.js` if using the export map
- ✅ `@skypack/export-map-test/simple`: should import `./simple.js`
- ✅ `@skypack/export-map-test/conditional`: should import **one** file in `./conditional`, depending on your criteria
- ✅ `@skypack/export-map-test/wildcard/css.css`: should succeed (as should `…/js.js` and `…/svg.svg`)
- ✅ `@skypack/export-map-test/wildcard-js/one`: should only be able to import any `.js` file without the extension (`one`, `two`, `three`)
- ❌ `@skypack/export-map-test/wildcard-js/css`: should fail (as should `svg`)
- ✅ `@skypack/export-map-test/package.json`: should succeed
- ❌ `@skypack/export-map-test/README.md`: should fail
