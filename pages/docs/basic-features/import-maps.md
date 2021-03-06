---
title: Import Maps
authors:
  - ije
---

# Import Maps

Aleph.js supports the [import maps](https://github.com/WICG/import-maps).

To use import maps, create a `import_map.json` file in the application root directory:
```json
{
  "imports": {
    "react": "https://esm.sh/react@16.13.1",
    ...
  }
}
```

then in your code:

```jsx
import React from "react"

export default function About() {
  return <h1>About</h1>
}
```

If you are using VS Code, please add below settings in the `.vscode/settings.json`:
```json
{
  "deno.enable": true,
  "deno.unstable": true,
  "deno.import_map": "./import_map.json"
}
```