# Caterpillar

Caterpillar is an awesome, simple console logger for [node.js](http://nodejs.org/). It supports grouping of messages, filtering log levels, colors, times, modules, custom formatters and custom transports.


## Example

### [examples/console.coffee](https://github.com/balupton/caterpillar.npm/blob/master/examples/console.coffee)

<img src="https://github.com/balupton/caterpillar.npm/raw/master/media/caterpillar-84x21.png"/>

``` coffeescript
# Requires
catepillar = require "#{__dirname}/../lib/caterpillar.coffee"

# Create
logger = new catepillar.Logger
	transports:
		level: 7
		formatter:
			module: module

# Logs
for own name,code of logger.config.levels
	logger.log name, "this is #{name}"

# Standard
logger.log 'this is awesome'

# Grouping
logger.config.autoFlush = false
logger.log ''
logger.log 'one'
logger.log 'two'
logger.log 'three'
setTimeout(
	-> logger.flush()
	3000
)
```


# Install

1. [Install Node.js](https://github.com/balupton/node/wiki/Installing-Node.js)

1. Install [CoffeeScript](http://jashkenas.github.com/coffee-script/)
		
		npm -g install coffee-script

1. Install Caterpillar

		npm install caterpillar


## Thanks

Uses the following:

- [RFC3164](http://www.faqs.org/rfcs/rfc3164.html) for the level codes and names
- [Mariusz Nowak's](https://github.com/medikoo) [CLI-Color](https://github.com/medikoo/cli-color)

Inspired by the following:

- [Alexander Dorofeev's](https://github.com/akaspin) [AIN](https://github.com/akaspin/ain)
- [TJ Holowaychuk's](https://github.com/visionmedia) [Log.js](https://github.com/visionmedia/log.js)
- [Igor Urminček's](https://github.com/igo) [NLogger](https://github.com/igo/nlogger)
- [SchizoDuckie's](https://github.com/SchizoDuckie) [Node-CLI](https://github.com/SchizoDuckie/Node-CLI/)


## License

Licensed under the [MIT License](http://creativecommons.org/licenses/MIT/)
Copyright 2011 [Benjamin Arthur Lupton](http://balupton.com)
