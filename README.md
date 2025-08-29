# Describe the Bug

Running `pnpm install --frozen-lockfile` does not fail when it should. Instead, it silently updates the pnpm-lock.yaml if a new package without dependencies is added.

## Expected Behavior

`pnpm install --frozen-lockfile` should fail with an error if the lockfile is out of sync, even when adding packages without dependencies.

## Reproduction steps

1. Clone <https://github.com/taewanseoul/pnpm-test>
2. Run `pnpm install --frozen-lockfile`
3. Observe that the `pnpm-lock.yaml` is updated instead of the command failing

## Environment

- pnpm: 10.15.0
- Node.js: 24.3.0
- macOS
