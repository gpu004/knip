# Repro: `@knip/create-config` misses pnpm workspace when `pnpm-workspace.yaml` uses CRLF

`pnpm-workspace.yaml` has CRLF line endings (kept by `.gitattributes`).

```sh
npm init @knip/config
```

With pnpm 9.15.9 (set in `packageManager`): `ERR_PNPM_ADDING_TO_ROOT`, the installer crashes.
With pnpm 10/11: install succeeds, but `knip.json` has no `workspaces` and a "Found package.json files in subdirectories" warning is printed.
