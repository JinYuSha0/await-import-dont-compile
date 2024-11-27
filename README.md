# AWAIT-IMPORT-DONT-COMPILE!

<div align="center">
<a href="https://www.npmjs.com/package/await-import-dont-compile"><img src="https://img.shields.io/npm/v/await-import-dont-compile.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/package/await-import-dont-compile"><img src="https://img.shields.io/npm/l/await-import-dont-compile.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/package/await-import-dont-compile"><img src="https://img.shields.io/npm/dm/await-import-dont-compile.svg" alt="NPM Downloads" /></a>
</div>

<center>Prevent typescript from compiling your import function</center>

```typescript
// original
await import("/my-module.js");

// After compilation
Promise.resolve().then(() => __importStar(require("/my-module.js")));

// Use AWAIT-IMPORT-DONT-COMPILE to prevent compilation
// and better organization of code
import awaitImport from "await-import-dont-compile";
import { pathToFileURL } from "url";

await awaitImport(pathToFileURL("/my-module.js").href);
```
