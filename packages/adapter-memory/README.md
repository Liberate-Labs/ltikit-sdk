# @ltikit/adapter-memory

In-memory `NonceStore` + `PlatformStore` for [LTIkit](https://github.com/Liberate-Labs/ltikit-sdk) —
**dev and tests only.** State is per-process and lost on restart, so it cannot enforce single-use
nonces across serverless invocations. Do not use in production.

Requires [`@ltikit/core`](https://www.npmjs.com/package/@ltikit/core).

```bash
npm i -D @ltikit/core @ltikit/adapter-memory
```

## Usage

```ts
import { MemoryNonceStore, MemoryPlatformStore } from '@ltikit/adapter-memory'

export const lti = createLti({
  keys: staticKeyStore({ /* ... */ }),
  nonces: new MemoryNonceStore(),
  platforms: new MemoryPlatformStore([/* seed Platform[] */]),
})
```

`MemoryPlatformStore` also implements the writable `MutablePlatformStore` contract, so **Dynamic
Registration** works out of the box in dev — the platform auto-onboards via `lti.dynamicRegistration.register(...)`.

## Docs

- [Storage adapters](https://liberate-labs.github.io/ltikit-sdk/guides/storage/)
- [Quickstart](https://liberate-labs.github.io/ltikit-sdk/getting-started/quickstart/)
- [API reference](https://liberate-labs.github.io/ltikit-sdk/api/adapter-memory/src/)

## Links

[Repository](https://github.com/Liberate-Labs/ltikit-sdk) ·
[Issues](https://github.com/Liberate-Labs/ltikit-sdk/issues) ·
[Need help?](https://liberate-labs.github.io/ltikit-sdk/support/) — paid setup/integration help available.

MIT
