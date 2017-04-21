# npmdoc-mocker-data-generator

#### api documentation for  mocker-data-generator (v2.0.0)  [![npm package](https://img.shields.io/npm/v/npmdoc-mocker-data-generator.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mocker-data-generator) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mocker-data-generator.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mocker-data-generator)

#### A simplified way to generate mock data, builds using a simple schema and with the FakerJs

[![NPM](https://nodei.co/npm/mocker-data-generator.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mocker-data-generator)

- [https://npmdoc.github.io/node-npmdoc-mocker-data-generator/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mocker-data-generator/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mocker-data-generator/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mocker-data-generator/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mocker-data-generator/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mocker-data-generator/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "mocker-data-generator",
    "version": "2.0.0",
    "description": "A simplified way to generate mock data, builds using a simple schema and with the FakerJs",
    "main": "build/main/index.js",
    "typings": "build/main/index.d.ts",
    "module": "build/module/index.js",
    "repository": "https://github.com/danibram/mocker-data-generator",
    "keywords": [
        "mock",
        "data",
        "faker",
        "fakerjs",
        "chance",
        "chancejs",
        "casual",
        "randexp",
        "json",
        "fake",
        "mocks",
        "massive",
        "generator"
    ],
    "author": {
        "name": "Daniel Biedma Ramos",
        "url": "dbr.io"
    },
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/danibram/mocker-data-generator/issues"
    },
    "scripts": {
        "info": "npm-scripts-info",
        "build": "trash build && tsc -p tsconfig.json && tsc -p config/tsconfig.module.json",
        "lint": "tslint src/**/*.ts",
        "unit": "yarn build && nyc ava",
        "check-coverage": "nyc check-coverage --lines 80 --functions 80 --branches 80",
        "test": "yarn lint && yarn unit && yarn check-coverage",
        "watch": "trash build && multiview [yarn watch:build] [yarn watch:unit]",
        "watch:build": "tsc -p tsconfig.json -w",
        "watch:unit": "tsc -p tsconfig.json && ava --watch --verbose",
        "cov": "yarn unit && yarn html-coverage && opn coverage/index.html",
        "html-coverage": "nyc report --reporter=html",
        "send-coverage": "nyc report --reporter=lcov > coverage.lcov && codecov",
        "docs": "typedoc src/index.ts --excludePrivate --mode file --theme minimal --out build/docs && opn build/docs/index.html",
        "docs:json": "typedoc --mode file --json build/docs/typedoc.json src/index.ts",
        "release": "standard-version"
    },
    "scripts-info": {
        "info": "Display information about the scripts",
        "build": "(Trash and re)build the library",
        "lint": "Lint all typescript source files",
        "unit": "Run unit tests",
        "test": "Lint and test the library",
        "watch": "Watch source files, rebuild library on changes, rerun relevant tests",
        "watch:build": "Watch source files, rebuild library on changes",
        "watch:unit": "Watch the build, rerun relevant tests on changes",
        "cov": "Run tests, generate the HTML coverage report, and open it in a browser",
        "html-coverage": "Output HTML test coverage report",
        "send-coverage": "Output lcov test coverage report and send it to codecov",
        "docs": "Generate API documentation and open it in a browser",
        "docs:json": "Generate API documentation in typedoc JSON format",
        "release": "Bump package.json version, update CHANGELOG.md, tag a release"
    },
    "devDependencies": {
        "@types/chance": "^0.7.31",
        "@types/faker": "^3.1.32",
        "@types/node": "^7.0.5",
        "ava": "^0.18.1",
        "codecov": "^1.0.1",
        "multiview": "^2.3.1",
        "npm-scripts-info": "^0.3.6",
        "nyc": "^10.0.0",
        "opn-cli": "^3.1.0",
        "standard-version": "^4.0.0",
        "trash-cli": "^1.4.0",
        "tslint": "^4.5.1",
        "tslint-config-standard": "^4.0.0",
        "typedoc": "^0.5.5",
        "typescript": "next",
        "tslib": "^1.5.0"
    },
    "dependencies": {
        "casual": "^1.5.11",
        "chance": "^1.0.0",
        "faker": "^4.1.0",
        "randexp": "^0.4.5"
    },
    "nyc": {
        "exclude": [
            "**/*.spec.js"
        ]
    },
    "ava": {
        "files": [
            "build/main/**/*.spec.js"
        ],
        "source": [
            "build/main/**/*"
        ]
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
