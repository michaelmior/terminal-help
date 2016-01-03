# Terminal Help

![](http://i1117.photobucket.com/albums/k594/thetutlage/poppins-1_zpsg867sqyl.png)

General purpose package to create a pretty help screen for your commands using an object. Terminal Help does not give you functionality to capture commands or flags from command line. It is a low-level library to create a help screen from an object.

- [Basic Usage](#basic-usage)
- [Grouped Commands](#grouped-commands)
- [Examples](#examples)

## Basic Usage

```javascript
const Help = require('terminal-help')
const packageFile = require('./package.json')
const options = {
  package: packageFile,
  commands: [
    {
      name: 'make:controller',
      description: 'Make a new controller file using its name'
    },
    {
      name: 'make:model',
      description: 'Make a new model file using its name'
    }
  ]
}
Help.menu(options)
```

Now the above will output

![Help Screen](http://i.imgur.com/giPRNuM.png?1)

## Grouped Commands

All commands are grouped with their namespace `:`, the above example shows all `make:` commands are grouped under make.

## Examples

Check out the examples directory to look at different examples.

`complete.js` shows a complete example with [yargs](https://github.com/bcoe/yargs)
