# @ltikit/hono

[Hono](https://hono.dev) route bindings for [LTIkit](https://github.com/Liberate-Labs/ltikit-sdk) — for edge
runtimes (Cloudflare Workers, Deno, Bun) or any Hono app.

**Pick one framework binding** (this, [`@ltikit/next`](https://www.npmjs.com/package/@ltikit/next),
or hand-rolled). Requires [`@ltikit/core`](https://www.npmjs.com/package/@ltikit/core) and
`hono` (peer dependency).

```bash
npm i @ltikit/core @ltikit/hono hono
```

## Usage

```ts
import { oidcLogin, launch, jwks } from '@ltikit/hono'

app.post('/api/lti/login', oidcLogin(lti, { redirectUri: `${APP_URL}/api/lti/launch` }))
app.post('/api/lti/launch', launch(lti, async (result, c) => c.redirect('/home')))
app.get('/.well-known/jwks.json', jwks(lti))
```

## Docs

- [Framework bindings](https://liberate-labs.github.io/ltikit-sdk/guides/frameworks/)
- [Quickstart](https://liberate-labs.github.io/ltikit-sdk/getting-started/quickstart/)
- [API reference](https://liberate-labs.github.io/ltikit-sdk/api/hono/src/)

## Links

[Repository](https://github.com/Liberate-Labs/ltikit-sdk) ·
[Issues](https://github.com/Liberate-Labs/ltikit-sdk/issues) ·
[Need help?](https://liberate-labs.github.io/ltikit-sdk/support/) — paid setup/integration help available.

MIT
