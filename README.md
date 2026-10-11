# Repro: knip GitHub Actions plugin, `checkout.path` + nested `working-directory`

```sh
npx knip@6.41.0
```

Actual: `Unused files (1) scripts/build.js`. Expected: no issues. `.github/workflows/ci.yml` runs `node build.js` in `repo/scripts` after checking out into `repo`.
