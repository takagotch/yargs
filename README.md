### yargs
---
https://github.com/yargs/yargs

```
npm i yargs --save
npm i yargs@next --save

./plunder.js --ships=4 --distance=22
./plunder.js --ships 12 --distance 98.7
```

```js
#!/usr/bin/env node
const argv = require('yargs').argv

if (argv.ships > 3 && argv.distance < 53.5) {
  console.log('Plunder more riffiwobbles!')
} else {
  console.log('Retreat from the xupptumblers!')
}

require('yargs')
  .command('serve [port]', 'start the server', (yargs) => {
    yargs
      .positional('port', {
        describe: 'port to bind on',
        default: 5000
      })
  }, (argv) => {
    if (argv.verbose) console.info(`start server on :${argv.port}`)
    serve(argv.port)
  })
  .optoin('verbose', {
    alias: 'v',
    default: false
  })
  .argv
```

```
```


