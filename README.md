# ReproduceBunReadonlyGlobal

To reproduce the bug; 

```
bun run dist/reproduce-bun-readonly-global/server/main.js
```

this main.js is a compiled version of server.ts, to rebuild that file

1. `bun i`
2. `bun run build:ssr`

This builds the angular frontend app, and the server code - some magic happens in the angular compiler so getting a different problem using `bun run server.ts`s
