# reka-ui Drawer SSR (no crash)

Same minimal example as `../vaul-ssr-test`, but built on reka-ui's native
`Drawer` primitive (`DrawerRoot` / `DrawerPortal` / `DrawerOverlay` /
`DrawerContent` from `reka-ui`, not `vaul-vue`) instead of vaul-vue.

## Run it

```bash
npm install
npm run build
node .output/server/index.mjs
curl -i http://localhost:3000/
```

Expect `HTTP/1.1 200` with the drawer content ("Hello from reka-ui")
present in the server-rendered HTML — no crash, unlike `../vaul-ssr-test`
which throws `document is not defined` under the identical
`default-open` + `force-mount` conditions.
