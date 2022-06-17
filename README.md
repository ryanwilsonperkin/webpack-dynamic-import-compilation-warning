Reproduction of a bug noted in Webpack https://github.com/webpack/webpack/issues/15960

Compiler outputs a warning message, but it should fail the compilation:

```
$ ./node_modules/.bin/webpack --mode production
asset main.js 3.05 KiB [compared for emit] [minimized] (name: main)
asset 717.js 153 bytes [compared for emit] [minimized]
runtime modules 7.9 KiB 10 modules
cacheable modules 45 bytes
  ./src/index.js 44 bytes [built] [code generated] [1 warning]
  ./src/foo.js 1 bytes [built] [code generated]

WARNING in ./src/index.js 1:7-34
Compilation error while processing magic comment(-s): /* webpackChunkName: foo */: foo is not defined
```
