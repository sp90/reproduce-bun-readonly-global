# ReproduceBunReadonlyGlobal

To reproduce the bug; 

```
bun run dist/reproduce-bun-readonly-global/server/main.js
```

this main.js is a compiled version of server.ts, to rebuild that file

1. `bun i`
2. `bun run build:ssr`

This builds the angular frontend app, and the server code - some magic happens in the angular compiler so getting a different problem using `bun run server.ts`s

### Error message

```
TypeError: Attempted to assign to readonly property.
      at setDomTypes (/Users/simon/Documents/dev/reproduce-bun-readonly-global/dist/reproduce-bun-readonly-global/server/main.js:1:2178309)
      at applyShims (/Users/simon/Documents/dev/reproduce-bun-readonly-global/dist/reproduce-bun-readonly-global/server/main.js:1:2821153)
      at /Users/simon/Documents/dev/reproduce-bun-readonly-global/dist/reproduce-bun-readonly-global/server/main.js:1:2821248
      at /Users/simon/Documents/dev/reproduce-bun-readonly-global/dist/reproduce-bun-readonly-global/server/main.js:1:2821259
      at /Users/simon/Documents/dev/reproduce-bun-readonly-global/dist/reproduce-bun-readonly-global/server/main.js:1:2874303
      at (eval) (/Users/simon/Documents/dev/reproduce-bun-readonly-global/dist/reproduce-bun-readonly-global/server/main.js:1:2874307)
```
