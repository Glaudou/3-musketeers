# cash

> This project converts some currencies.

## I) Installations

1) Go to your folder where your files lie using the shell command
```sh
â¯ cd /path/to/worskpace/3-musketeers/cash
```

2) Install all the dependencies needed in the local folder using the command
```sh
â¯ npm i
```

## III) Usage

```sh
â¯ node bin/index.js
```

```js
const Conf = require('conf');
const meow = require('meow');
const chalk = require('chalk');
const cash = require('./cash.js');

const config = new Conf();
const argv = process.argv.slice(2);

const {DEFAULT_TO_CURRENCIES} = require('./constants');

const cli = meow(`
	Usage
		$ cash <amount> <from> <to>
		$ cash <options>
	Options
		--set -s 			Set default currencies
	Examples
		$ cash 10 usd eur pln
		$ cash --set usd aud
`);
```
