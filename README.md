# palette

Hex palette parsing, interpolation, and deterministic selection.

A [KEEL](https://github.com/Ravonus/keel-modules) module: strict, readable
TypeScript that the platform minifies into the exact bytes published on chain,
with a hash-linked receipt binding the two.

## Verify it yourself

```bash
keel module build .
```

The build is deterministic, so it must print exactly:

```
output digest:  0x785ac9e4d8641662862703d3d3d7b97c6085528e03714ee331979619db2108da
```

If it prints anything else, the readable source in this repository is not the
source the published bytes were built from, and you should not trust it. You do
not have to take anyone's word for that, which is the entire point.

Run `keel module test .` to run the vectors in `test/vectors.mjs` against
both the readable source and the minified bytes.

## Where this comes from

This repository is a mirror. The source of truth is
[`keel-web3/render/palette`](https://github.com/Ravonus/keel-modules/tree/master/modules/keel-web3/render/palette)
in the keel-modules monorepo, at commit `c2e15084c24c7f8d4187f06b3a85347d6f4a0354`. Both trees build
to the same digest above; the mirror exists so this module can be depended on,
starred, and forked on its own.

## Licence

MIT. See LICENSE.
