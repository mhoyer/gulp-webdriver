gulp-webdriver [![Build Status](https://travis-ci.org/webdriverio/gulp-webdriver.svg?branch=master)](https://travis-ci.org/webdriverio/gulp-webdriver) [![Join the chat at https://gitter.im/webdriverio/gulp-webdriver](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/webdriverio/gulp-webdriver?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
==============

> gulp-webdriver is a gulp plugin to run selenium tests with the [WebdriverIO](http://webdriver.io) testrunner

## Install

```shell
npm install gulp-webdriver --save-dev
```

## Usage

You can run WebdriverIO locally running this simple task:

```js
gulp.task('test:e2e', function() {
    return gulp.src('wdio.conf.js').pipe(webdriver());
});
```

gulp-webdriver makes the wdio testrunner easy accessible and allows you to run multiple config files
sequentially. If desired you can pass additional arguments to the wdio command to specify your test.
You can find all available options [here](http://webdriver.io/guide/testrunner/gettingstarted.html)
or by executin `$ wdio --help` (if you have WebdriverIO installed globally).

```js
gulp.task('test:e2e', function() {
    return gulp.src('wdio.conf.js').pipe(webdriver({
        logLevel: 'verbose',
        waitforTimeout: 10000,
        reporter: 'spec'
    }));
});
```

## Contributing
Please fork, add specs, and send pull requests! In lieu of a formal styleguide, take care to
maintain the existing coding style.

## Release History
* 2015-06-22   v0.1.0   first release
* 2015-06-22   v0.1.1   fixed package.json
* 2015-09-03   v1.0.0   let gulp-webdriver be a simple tool to run tests with the wdio test runner
