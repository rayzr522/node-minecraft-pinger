# minecraft-pinger

[![js-standard-style](https://img.shields.io/badge/code%20style-standard-yellowgreen.svg)](http://standardjs.com/)
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE.md)

> A promise-based minecraft pinger in Node.js

## Installation

```bash
$ npm install --save-prod '@rayzr/minecraft-pinger'
```

## TODOs

- [x] Calculate latency in milliseconds
- [x] Resolve SRV dns entry
- [ ] Able to ping servers prior version 1.6

## Example

```javascript
const pinger = require('@rayzr/minecraft-pinger')

// Promise
pinger.pingPromise('localhost', 25565)
  .then(console.log)
  .catch(console.error)

// Callback
pinger.ping('localhost', 25565, (error, result) => {
  if (error) return console.error(error)
  console.log(result)
})
```

## License

[MIT](LICENSE.md)
