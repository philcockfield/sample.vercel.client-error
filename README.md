# Error Reproduction

From here on the website (https://vercel.com/download):

![img](https://user-images.githubusercontent.com/185555/86195098-467f4d00-bba4-11ea-94f2-edd1559cc17a.png)

there is a link to the [repo here](https://github.com/vercel/vercel/tree/master/packages/now-client).

Which causes the following error:

![error](https://user-images.githubusercontent.com/185555/86195103-4a12d400-bba4-11ea-9b6f-f23e843469c8.png)

This is reproduced within this repo by running:

```
yarn install
node .
```

Ass you'll see, there is nothing really going on in this repo other than referencing the library and attempting to import it:

```json
// package.json
{
  "name": "foo",
  "version": "1.0.0",
  "main": "index.js",
  "dependencies": {
    "@vercel/client": "^8.1.0"
  }
}
```

and the main entry:

```js
const client = require("@vercel/client");
console.log(client);
```

Note: This has been lodged on email support and can be found as ticket number `#55242`

Go you guys! Love ya 👋
