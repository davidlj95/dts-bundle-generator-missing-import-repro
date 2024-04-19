To reproduce the bug:

```shell
pnpm install
dts-bundle-generator index.d.ts --out-file bundled.d.ts
```

Output is

```text
Compiling input files...
Processing index.d.ts
Writing index.d.ts -> bundled.d.ts
Checking generated files...
bundled.d.ts(7,15): error TS2503: Cannot find namespace 'i0'.
bundled.d.ts(8,15): error TS2503: Cannot find namespace 'i0'.
bundled.d.ts(9,15): error TS2503: Cannot find namespace 'i0'.

Error: Failed to check some of generated bundles, check error messages above
```

This worked in previous `dts-bundle-generator` (`9.3.1`) but not in new ones (`9.4.0` / `9.5.0`)
