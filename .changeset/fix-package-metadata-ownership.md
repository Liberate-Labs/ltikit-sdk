---
"@ltikit/core": patch
"@ltikit/next": patch
"@ltikit/adapter-supabase": patch
"@ltikit/adapter-memory": patch
"@ltikit/adapter-redis": patch
"@ltikit/hono": patch
---

Correct package metadata (`repository`, `homepage`, `bugs`, `author`) to point at the
`Liberate-Labs/ltikit-sdk` repo and org contact — npm still served the previous personal-repo
metadata from the prior publish. No functional changes.
