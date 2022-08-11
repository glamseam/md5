# Description

This repository is a clone of [cotag/ts-md5](https://github.com/cotag/ts-md5)

Thank you.

# Introduction

A MD5 implementation for TypeScript.

Both `.cjs` and `.mjs` are exported.

# Usage

## Install
`npm i @d-gs/md5`

or

`pnpm add @d-gs/md5`

## Basic Hashing

1. Import the class
    * `import { Md5 } from '@d-gs/md5';`
2. Hash some things
    * `Md5.hashStr('blah blah blah')` => hex:string
    * `Md5.hashStr('blah blah blah', true)` => raw:Int32Array(4)
    * `Md5.hashAsciiStr('blah blah blah')` => hex:string
    * `Md5.hashAsciiStr('blah blah blah', true)` => raw:Int32Array(4)

For more complex uses:

```typescript
import { Md5 } from '@d-gs/md5'

md5 = new Md5();

// Append incrementally your file or other input
// Methods are chainable
md5.appendStr('somestring')
    .appendAsciiStr('a different string')
    .appendByteArray(blob);

// Generate the MD5 hex string
md5.end();
```
