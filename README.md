# The replication

This repo demonstrates [this bug](https://github.com/cloudflare/workerd/issues/2025) with `.getWebSocketAutoResponseTimestamp()` (or `.gWSART()`).

📽️ [Video demo](https://share.cleanshot.com/nzVS2sMSHgz7YLcrTdXZ)

### It works locally...

1. Check out this branch.
2. `npm i`
3. Run `npm run dev` (this will run the server locally)
4. Run `bun run client-script.ts`

### ...however it does not work on Cloudflare infrastructure

Simplest:

1. Check out this branch.
2. `npm i`
3. Run `npm run dev` (this will run the server locally)
4. Switch to "remote" mode, by pressing `l`
5. Run `bun run client-script.ts`

Alternatively:

1. Check out this branch.
2. `npm i`
3. Deploy this to Cloudflare
4. Change `CONNECTION_STRING` in `client-script.ts` to the deployment URL.
5. Run `bun run client-script.ts`
