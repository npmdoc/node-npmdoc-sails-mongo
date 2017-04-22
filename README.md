# npmdoc-sails-mongo

#### api documentation for  [sails-mongo (v0.12.2)](https://github.com/balderdashy/sails-mongo#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-sails-mongo.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sails-mongo) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sails-mongo.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sails-mongo)

#### Mongo DB adapter for Sails.js

[![NPM](https://nodei.co/npm/sails-mongo.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sails-mongo)

- [https://npmdoc.github.io/node-npmdoc-sails-mongo/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/balderdashy/sails-mongo/issues"
    },
    "contributors": [
        {
            "name": "Cody Stoltman"
        },
        {
            "name": "Zolmeister"
        },
        {
            "name": "Robin Persson"
        },
        {
            "name": "Ted Kulp"
        },
        {
            "name": "Andy Pham"
        }
    ],
    "dependencies": {
        "@sailshq/lodash": "3.10.2",
        "async": "2.0.1",
        "mongodb": "2.1.20",
        "validator": "4.5.1",
        "waterline-cursor": "0.0.7",
        "waterline-errors": "0.10.1"
    },
    "description": "Mongo DB adapter for Sails.js",
    "devDependencies": {
        "captains-log": "^1.0.2",
        "mocha": "3.0.2",
        "waterline-adapter-tests": "~0.12.1"
    },
    "directories": {},
    "dist": {
        "shasum": "475b9e508d380f8787a0e6b1dfebbd607f4f66e3",
        "tarball": "https://registry.npmjs.org/sails-mongo/-/sails-mongo-0.12.2.tgz"
    },
    "gitHead": "feb4760daa65d238765bfa39f6be3cd8b1e6805d",
    "homepage": "https://github.com/balderdashy/sails-mongo#readme",
    "keywords": [
        "mongo",
        "mongodb",
        "orm",
        "waterline",
        "sails"
    ],
    "license": "MIT",
    "main": "./lib/adapter.js",
    "maintainers": [
        {
            "name": "balderdashy"
        },
        {
            "name": "mikermcneil"
        },
        {
            "name": "particlebanana"
        },
        {
            "name": "sgress454"
        },
        {
            "name": "tedkulp"
        }
    ],
    "name": "sails-mongo",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/balderdashy/sails-mongo.git"
    },
    "scripts": {
        "docker": "docker-compose run adapter bash",
        "test": "make test"
    },
    "version": "0.12.2",
    "waterlineAdapter": {
        "waterlineVersion": "~0.10.0",
        "interfaces": [
            "semantic",
            "queryable",
            "associations"
        ],
        "features": [
            "cross-adapter"
        ]
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
