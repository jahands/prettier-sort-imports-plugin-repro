# prettier-sort-imports-plugin-repro

To repro:

```sh
git clone https://github.com/jahands/prettier-sort-imports-plugin-repro.git
cd prettier-sort-imports-plugin-repro
npm i
npm run format
```

Result:

```
$ npm run format

> prettier-sort-imports-plugin-repro@1.0.0 format
> prettier --write .

.prettierrc.cjs 17ms (unchanged)
example.toml
[error] example.toml: Error: Error: prettier-plugin-ember-template-tag could not be loaded.  Is it installed?
[error]     at M.format (/Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/@taplo/lib/dist/index.js:2:35638065)
[error]     at format (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier-plugin-toml/lib/index.js:10:21)
[error]     at async parse5 (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier/index.mjs:16731:11)
[error]     at async coreFormat (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier/index.mjs:17287:25)
[error]     at async formatWithCursor (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier/index.mjs:17504:14)
[error]     at async formatFiles (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier/internal/legacy-cli.mjs:4279:18)
[error]     at async main (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier/internal/legacy-cli.mjs:4698:5)
[error]     at async Module.run (file:///Users/jh/src/prettier-sort-imports-plugin-repro/node_modules/prettier/internal/legacy-cli.mjs:4641:5)
package-lock.json 15ms (unchanged)
package.json 1ms (unchanged)
README.md 13ms (unchanged)
```
