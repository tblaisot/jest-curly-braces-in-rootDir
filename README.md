Test don't seem to run if the app's root path contains curly braces on windows and testMatch's globs interpolate `<rootDir>`.

As an example, the following won't run any tests:

```sh
cd "with-{curly-braces}"
npm install
npm test
```

This bug can be reproduced with path containing curly-braces from the start like `/{folder-with-curly}`

However, this finds tests successfully:

```sh
cd without-curly-brace
npm install
npm test
```

And this too:


```sh
cd with-curly-brace-in-subfolder
npm install
npm test
```
