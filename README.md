# @insurgent/export-map-test

Package that exposes various entry points via [`package.json`'s `exports` field](https://nodejs.org/api/packages.html#packages_package_entry_points) for testing purposes.

Each file contains specific content to be able to test the loaded module value.

```shell
npm i @insurgent/export-map-test
```

### Conditions:

- ✅ `@insurgent/export-map-test`: should import `./main.js`
- ✅ `@insurgent/export-map-test/simple`: should import `./simple.js`
- ✅ `@insurgent/export-map-test/conditional`: should import **one** file in `./conditional`, depending on your criteria
- ✅ `@insurgent/export-map-test/wildcard/css.css`: should succeed (as should `js.js` and `svg.svg`)
- ✅ `@insurgent/export-map-test/wildcard-js/one`: should only be able to import any `.js` file without the extension (`one`, `two`, `three`)
- ❌ `@insurgent/export-map-test/wildcard-js/css`: should fail (as should `svg`)
- ✅ `@insurgent/export-map-test/package.json`: should succeed
- ❌ `@insurgent/export-map-test/README.md`: should fail
