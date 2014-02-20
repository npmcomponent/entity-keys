*This repository is a mirror of the [component](http://component.io) module [entity/keys](http://github.com/entity/keys). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/entity-keys`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# keys

bind to a key map

## Installing

`component install entity/keys`

## Example

```js
var map = {
  37: 'left',
  38: 'up',
  39: 'right',
  40: 'down'
};

var keys = require('keys')(map);

document.body.onkeydown = keys.onkeydown;
document.body.onkeyup = keys.onkeyup;

var log = console.log.bind(console);

keys.on('keydown', log);
keys.on('keyup', log);
keys.on('change', log);
```

## API

### keys(map)

Creates key `map` handler.

`map` is an object with keycode property names
where their corresponding values are emitted
on keyup/down events.

## Events

- `keydown` (event, key)
- `keyup` (event, key)
- `change` (event, key, state)

## License

MIT
