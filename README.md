# next-absolute-url

> Get the protocol and host for the absolute URL of your Next.js app (and optionally set a dev url)

This module enables you to easily get the protocol and host of your Next.js app, both on the server and the client.  Optionally, you can set a localhost variable, which is useful for local development if you have local lambda functions running on a different port.

## Usage

```js
import absoluteUrl from 'next-absolute-url'
const { protocol, host } = absoluteUrl(req, 'localhost:8004')
const apiURL = `${protocol}//${host}/api/job.js`
```

If you deployed your Next.js app with `now` the `apiURL` will be something like `https://your-app.now.sh/api/job.js`.

However, if you are running the app locally the `apiURL` will be `http://localhost:8004/api/job.js` instead.


## Install

With [npm](https://npmjs.org/) installed, run

```
$ npm install next-absolute-url
```

MIT

