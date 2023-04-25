
Adding `"type": "module"` to `package.json` re-creates the error, if it's not present and uses require, cypress works as expected.

To recreate the issue run the following commands with node `20`

```sh
npm install
npm run test:e2e
```

This error should be present in the console 

```
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9238) ExperimentalWarning: Custom ESM Loaders is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9238) ExperimentalWarning: Custom ESM Loaders is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9238) ExperimentalWarning: Custom ESM Loaders is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9238) ExperimentalWarning: Custom ESM Loaders is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9238) ExperimentalWarning: Custom ESM Loaders is an experimental feature and might change at any time
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9238) ExperimentalWarning: Custom ESM Loaders is an experimental feature and might change at any time
```

Using node `19` has shows the error but is less frequent.