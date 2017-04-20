# npmtest-react-highcharts

#### basic test coverage for  [react-highcharts (v11.5.0)](https://github.com/kirjs/react-highcharts#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-react-highcharts.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-react-highcharts) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-react-highcharts.svg)](https://travis-ci.org/npmtest/node-npmtest-react-highcharts)

#### React wrapper for highcharts

[![NPM](https://nodei.co/npm/react-highcharts.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-highcharts)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-react-highcharts/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-highcharts/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-react-highcharts/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-react-highcharts/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-react-highcharts/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-react-highcharts/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-react-highcharts/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-react-highcharts/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-react-highcharts/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-highcharts/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-react-highcharts/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-react-highcharts/build/test-report.html](https://npmtest.github.io/node-npmtest-react-highcharts/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-react-highcharts/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-react-highcharts/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-react-highcharts/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-react-highcharts/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-highcharts/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-highcharts/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-react-highcharts/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-react-highcharts/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Kirill Cherkashin"
    },
    "bugs": {
        "url": "https://github.com/kirjs/react-highcharts/issues"
    },
    "dependencies": {
        "highcharts": "^5.0.0"
    },
    "description": "React wrapper for highcharts",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-core": "^6.21.0",
        "babel-loader": "^6.2.10",
        "babel-preset-es2015": "^6.18.0",
        "babel-preset-react": "^6.16.0",
        "babel-preset-stage-2": "^6.18.0",
        "exports-loader": "^0.6.2",
        "file-loader": "^0.9.0",
        "highlight.js": "^9.3.0",
        "imports-loader": "^0.6.4",
        "jsdom": "^9.9.1",
        "mocha": "^3.2.0",
        "mock-require": "^1.3.0",
        "nightwatch": "^0.9.6",
        "raw-loader": "^0.5.1",
        "react": "^15.0.0",
        "react-addons-test-utils": "^15.4.1",
        "react-dom": "^15.0.0",
        "react-highlight": "^0.9.0",
        "sinon": "^1.17.6",
        "webpack": "^1.14.0",
        "webpack-dev-server": "^1.10.1"
    },
    "directories": {},
    "dist": {
        "shasum": "2812cdc56ef1057e59cbc9c4dbed79b72d8505ae",
        "tarball": "https://registry.npmjs.org/react-highcharts/-/react-highcharts-11.5.0.tgz"
    },
    "gitHead": "191a9253f48dc1dcfc2f787f1ca93985b19cdb60",
    "homepage": "https://github.com/kirjs/react-highcharts#readme",
    "keywords": [
        "chart",
        "react",
        "highcharts",
        "graph"
    ],
    "license": "MIT",
    "main": "dist/ReactHighcharts.js",
    "maintainers": [
        {
            "name": "kirjs"
        }
    ],
    "name": "react-highcharts",
    "optionalDependencies": {},
    "peerDependencies": {
        "react": "~0.14 || ^15.0.0",
        "react-dom": "~0.14 || ^15.0.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/kirjs/react-highcharts.git"
    },
    "scripts": {
        "build": "webpack && webpack -p && webpack -b && webpack -p -b",
        "copy-bundles": "sh ./src/copy-bundles.sh",
        "demo": "cd demo && webpack &&  sh generate-contents.sh && ../node_modules/.bin/webpack-dev-server --content-base dist/",
        "deploy-demo": "./demo/deploy.sh",
        "e2e": "nightwatch test/e2e/e2e-launcher.js -e local --config nightwatch.js ",
        "e2e-sc": "nightwatch test/e2e/e2e-launcher.js -e saucelabs --config nightwatch.js ",
        "generate-modules": "(cd src; sh ./generate-modules.sh)",
        "postversion": "git push && git push --tags",
        "prepublish": "npm run build && npm run copy-bundles",
        "preversion": "npm test",
        "test": "webpack && mocha test/unit",
        "version": "npm run prepublish"
    },
    "version": "11.5.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
