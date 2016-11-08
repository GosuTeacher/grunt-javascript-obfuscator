# grunt-javascript-obfuscator

[![Build Status](https://travis-ci.org/tomasz-oponowicz/grunt-javascript-obfuscator.svg?branch=master)](https://travis-ci.org/tomasz-oponowicz/grunt-javascript-obfuscator)

> Obfuscates JavaScript files using amazing [javascript-obfuscator](https://github.com/javascript-obfuscator/javascript-obfuscator).

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin and _javascript-obfuscator_ with this command:

```shell
npm install grunt-javascript-obfuscator javascript-obfuscator --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-javascript-obfuscator');
```

## The "javascript_obfuscator" task

### Overview
In your project's Gruntfile, add a section named `javascript_obfuscator` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  javascript_obfuscator: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

### Options

Options are passed directly to _javascript-obfuscator_. Please visit [documentation of the project](https://github.com/javascript-obfuscator/javascript-obfuscator) for a complete list of options.

### Usage Examples

#### Default Options

In this example, the default options are used to obfuscate scripts:

```js
grunt.initConfig({
  javascript_obfuscator: {
    options: {
      /* Default options */
    },
    files: {
      'dist/obfuscated.js': ['src/module1.js', 'src/module2.js']
    },
  },
});
```

#### Custom Options

In this example, custom options are used to obfuscate scripts. `debugProtection` makes it almost impossible to use the console tab of the Developer Tools:

```js
grunt.initConfig({
  javascript_obfuscator: {
    options: {
      debugProtection: true,
      debugProtectionInterval: true
    },
    files: {
      'dist/obfuscated.js': ['src/module1.js', 'src/module2.js']
    },
  },
});
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History

 * 2016-11-08   v1.0.0   First release.
