Test don't seem to run if the app's root path contains parentheses and testMatch's globs interpolate `<rootDir>`.

As an example, the following won't run any tests:

```sh
cd with-\(parens\)
npm install
npm test
```

However, this finds tests successfully:

```sh
cd without-parens
npm install
npm test
```
