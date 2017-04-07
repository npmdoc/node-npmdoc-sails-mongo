# api documentation for  [sails-mongo (v0.12.2)](https://github.com/balderdashy/sails-mongo#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-sails-mongo.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sails-mongo) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sails-mongo.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sails-mongo)
#### Mongo DB adapter for Sails.js

[![NPM](https://nodei.co/npm/sails-mongo.png?downloads=true)](https://www.npmjs.com/package/sails-mongo)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-sails-mongo%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sails-mongo/build/apidoc.html)

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
            "name": "Cody Stoltman",
            "email": "particlebanana@gmail.com"
        },
        {
            "name": "Zolmeister",
            "email": "zolikahan@gmail.com"
        },
        {
            "name": "Robin Persson",
            "email": "rprssn@gmail.com"
        },
        {
            "name": "Ted Kulp",
            "email": "github@wishy.org"
        },
        {
            "name": "Andy Pham",
            "email": "andyphamhung@gmail.com"
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
            "name": "balderdashy",
            "email": "mike@balderdash.co"
        },
        {
            "name": "mikermcneil",
            "email": "michael.r.mcneil@gmail.com"
        },
        {
            "name": "particlebanana",
            "email": "particlebanana@gmail.com"
        },
        {
            "name": "sgress454",
            "email": "sgress454@treeline.io"
        },
        {
            "name": "tedkulp",
            "email": "ted@tedkulp.com"
        }
    ],
    "name": "sails-mongo",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    }
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sails-mongo](#apidoc.module.sails-mongo)
1.  boolean <span class="apidocSignatureSpan">sails-mongo.</span>syncable
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>collection (definition, connection)](#apidoc.element.sails-mongo.collection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>connection (config, cb)](#apidoc.element.sails-mongo.connection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>count (connectionName, collectionName, options, cb)](#apidoc.element.sails-mongo.count)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>create (connectionName, collectionName, data, cb)](#apidoc.element.sails-mongo.create)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>createEach (connectionName, collectionName, data, cb)](#apidoc.element.sails-mongo.createEach)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>define (connectionName, collectionName, definition, cb)](#apidoc.element.sails-mongo.define)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>describe (connectionName, collectionName, cb)](#apidoc.element.sails-mongo.describe)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>destroy (connectionName, collectionName, options, cb)](#apidoc.element.sails-mongo.destroy)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>document (values, schema)](#apidoc.element.sails-mongo.document)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>drop (connectionName, collectionName, relations, cb)](#apidoc.element.sails-mongo.drop)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>find (connectionName, collectionName, options, cb)](#apidoc.element.sails-mongo.find)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>join (connectionName, collectionName, criteria, cb)](#apidoc.element.sails-mongo.join)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>native (connectionName, collectionName, cb)](#apidoc.element.sails-mongo.native)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>registerConnection (connection, collections, cb)](#apidoc.element.sails-mongo.registerConnection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>stream (connectionName, collectionName, options, stream)](#apidoc.element.sails-mongo.stream)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>teardown (conn, cb)](#apidoc.element.sails-mongo.teardown)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>update (connectionName, collectionName, options, values, cb)](#apidoc.element.sails-mongo.update)
1.  object <span class="apidocSignatureSpan">sails-mongo.</span>collection.prototype
1.  object <span class="apidocSignatureSpan">sails-mongo.</span>connection.prototype
1.  object <span class="apidocSignatureSpan">sails-mongo.</span>defaults
1.  object <span class="apidocSignatureSpan">sails-mongo.</span>document.prototype
1.  object <span class="apidocSignatureSpan">sails-mongo.</span>mongo
1.  object <span class="apidocSignatureSpan">sails-mongo.</span>utils
1.  string <span class="apidocSignatureSpan">sails-mongo.</span>identity
1.  string <span class="apidocSignatureSpan">sails-mongo.</span>pkFormat

#### [module sails-mongo.collection](#apidoc.module.sails-mongo.collection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>collection (definition, connection)](#apidoc.element.sails-mongo.collection.collection)

#### [module sails-mongo.collection.prototype](#apidoc.module.sails-mongo.collection.prototype)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>_buildIndexes ()](#apidoc.element.sails-mongo.collection.prototype._buildIndexes)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>_getPK ()](#apidoc.element.sails-mongo.collection.prototype._getPK)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>_parseDefinition (definition)](#apidoc.element.sails-mongo.collection.prototype._parseDefinition)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>count (criteria, cb)](#apidoc.element.sails-mongo.collection.prototype.count)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>destroy (criteria, cb)](#apidoc.element.sails-mongo.collection.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>find (criteria, cb)](#apidoc.element.sails-mongo.collection.prototype.find)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>insert (values, cb)](#apidoc.element.sails-mongo.collection.prototype.insert)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>stream (criteria, stream)](#apidoc.element.sails-mongo.collection.prototype.stream)
1.  [function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>update (criteria, values, cb)](#apidoc.element.sails-mongo.collection.prototype.update)

#### [module sails-mongo.connection](#apidoc.module.sails-mongo.connection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>connection (config, cb)](#apidoc.element.sails-mongo.connection.connection)

#### [module sails-mongo.connection.prototype](#apidoc.module.sails-mongo.connection.prototype)
1.  [function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>_buildConnection (cb)](#apidoc.element.sails-mongo.connection.prototype._buildConnection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>_ensureIndexes (collection, indexes, cb)](#apidoc.element.sails-mongo.connection.prototype._ensureIndexes)
1.  [function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>createCollection (name, collection, cb)](#apidoc.element.sails-mongo.connection.prototype.createCollection)
1.  [function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>dropCollection (name, cb)](#apidoc.element.sails-mongo.connection.prototype.dropCollection)

#### [module sails-mongo.document](#apidoc.module.sails-mongo.document)
1.  [function <span class="apidocSignatureSpan">sails-mongo.</span>document (values, schema)](#apidoc.element.sails-mongo.document.document)

#### [module sails-mongo.document.prototype](#apidoc.module.sails-mongo.document.prototype)
1.  [function <span class="apidocSignatureSpan">sails-mongo.document.prototype.</span>normalizeId (values)](#apidoc.element.sails-mongo.document.prototype.normalizeId)
1.  [function <span class="apidocSignatureSpan">sails-mongo.document.prototype.</span>serializeValues (values)](#apidoc.element.sails-mongo.document.prototype.serializeValues)
1.  [function <span class="apidocSignatureSpan">sails-mongo.document.prototype.</span>setValues (values)](#apidoc.element.sails-mongo.document.prototype.setValues)

#### [module sails-mongo.mongo](#apidoc.module.sails-mongo.mongo)
1.  [function <span class="apidocSignatureSpan">sails-mongo.mongo.</span>objectId (id)](#apidoc.element.sails-mongo.mongo.objectId)

#### [module sails-mongo.utils](#apidoc.module.sails-mongo.utils)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>_rewriteIds (model, schema)](#apidoc.element.sails-mongo.utils._rewriteIds)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>caseInsensitive (val)](#apidoc.element.sails-mongo.utils.caseInsensitive)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>clarifyError (err)](#apidoc.element.sails-mongo.utils.clarifyError)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>matchMongoId (id)](#apidoc.element.sails-mongo.utils.matchMongoId)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>normalizeResults (models, schema)](#apidoc.element.sails-mongo.utils.normalizeResults)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>parseUrl (config)](#apidoc.element.sails-mongo.utils.parseUrl)
1.  [function <span class="apidocSignatureSpan">sails-mongo.utils.</span>rewriteIds (models, schema)](#apidoc.element.sails-mongo.utils.rewriteIds)
1.  object <span class="apidocSignatureSpan">sails-mongo.utils.</span>object



# <a name="apidoc.module.sails-mongo"></a>[module sails-mongo](#apidoc.module.sails-mongo)

#### <a name="apidoc.element.sails-mongo.collection"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>collection (definition, connection)](#apidoc.element.sails-mongo.collection)
- description and source-code
```javascript
function Collection(definition, connection) {

  // Set an identity for this collection
  this.identity = '';

  // Hold Schema Information
  this.schema = null;

  // Hold a reference to an active connection
  this.connection = connection;

  // Hold the config object
  var connectionConfig = connection.config || {};
  this.config = _.extend({}, connectionConfig.wlNext);

  // Hold Indexes
  this.indexes = [];

  // Parse the definition into collection attributes
  this._parseDefinition(definition);

  // Build an indexes dictionary
  this._buildIndexes();

  return this;
}
```
- example usage
```shell
...
// Catch errors from building query and return to the callback
try {
  query = new Query(criteria, this.schema, this.config);
} catch(err) {
  return cb(err);
}

var collection = this.connection.db.collection(self.identity);

// Check for aggregate query
if(query.aggregate) {
  var aggregate = [
    { '$match': query.criteria.where || {} },
    { '$group': query.aggregateGroup }
  ];
...
```

#### <a name="apidoc.element.sails-mongo.connection"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>connection (config, cb)](#apidoc.element.sails-mongo.connection)
- description and source-code
```javascript
function Connection(config, cb) {
  var self = this;

  // Hold the config object
  this.config = config || {};

  // Build Database connection
  this._buildConnection(function(err, db) {
    if(err) return cb(err);
    if(!db) return cb(new Error('no db object'));

    // Store the DB object
    self.db = db;

    // Return the connection
    cb(null, self);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.count"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>count (connectionName, collectionName, options, cb)](#apidoc.element.sails-mongo.count)
- description and source-code
```javascript
count = function (connectionName, collectionName, options, cb) {
  options = options || {};
  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Find matching documents and return the count
  collection.count(options, function(err, results) {
    if(err) return cb(err);
    cb(null, results);
  });
}
```
- example usage
```shell
...
  // Catch errors build query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return cb(err);
  }

  this.connection.db.collection(this.identity).count(query.criteria.where, function(err, count) {
    if (err) return cb(err);
    cb(null, count);
  });
};


/////////////////////////////////////////////////////////////////////////////////
...
```

#### <a name="apidoc.element.sails-mongo.create"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>create (connectionName, collectionName, data, cb)](#apidoc.element.sails-mongo.create)
- description and source-code
```javascript
create = function (connectionName, collectionName, data, cb) {

  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Insert a new document into the collection
  collection.insert(data, function(err, results) {
    if(err) return cb(utils.clarifyError(err));
    cb(null, results[0]);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.createEach"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>createEach (connectionName, collectionName, data, cb)](#apidoc.element.sails-mongo.createEach)
- description and source-code
```javascript
createEach = function (connectionName, collectionName, data, cb) {

  if (data.length === 0) {return cb(null, []);}

  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Insert a new document into the collection
  collection.insert(data, function(err, results) {
    if(err) return cb(utils.clarifyError(err));
    cb(null, results);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.define"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>define (connectionName, collectionName, definition, cb)](#apidoc.element.sails-mongo.define)
- description and source-code
```javascript
define = function (connectionName, collectionName, definition, cb) {

  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Create the collection and indexes
  connectionObject.connection.createCollection(collectionName, collection, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.describe"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>describe (connectionName, collectionName, cb)](#apidoc.element.sails-mongo.describe)
- description and source-code
```javascript
describe = function (connectionName, collectionName, cb) {

  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];
  var schema = collection.schema;
  var names = connectionObject.connection.db.listCollections(collectionName);
  if(names.length > 0) return cb(null, schema);
  cb();

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.destroy"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>destroy (connectionName, collectionName, options, cb)](#apidoc.element.sails-mongo.destroy)
- description and source-code
```javascript
destroy = function (connectionName, collectionName, options, cb) {
  options = options || {};
  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Find matching documents
  collection.find(options, function(err, results) {
    if(err) return cb(err);

    // Destroy matching documents
    collection.destroy(options, function(err) {
      if(err) return cb(err);
      cb(null, results);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.document"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>document (values, schema)](#apidoc.element.sails-mongo.document)
- description and source-code
```javascript
function Document(values, schema) {

  // Keep track of the current document's values
  this.values = {};

  // Grab the schema for normalizing values
  this.schema = schema || {};

  // If values were passed in, use the setter
  if(values) this.values = this.setValues(values);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.drop"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>drop (connectionName, collectionName, relations, cb)](#apidoc.element.sails-mongo.drop)
- description and source-code
```javascript
drop = function (connectionName, collectionName, relations, cb) {

  if(typeof relations === 'function') {
    cb = relations;
    relations = [];
  }

  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Drop the collection and indexes
  connectionObject.connection.dropCollection(collectionName, function(err) {

    // Don't error if droping a collection which doesn't exist
    if(err && err.errmsg === 'ns not found') return cb();
    if(err) return cb(err);
    cb();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.find"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>find (connectionName, collectionName, options, cb)](#apidoc.element.sails-mongo.find)
- description and source-code
```javascript
find = function (connectionName, collectionName, options, cb) {
  options = options || {};
  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Find all matching documents
  collection.find(options, function(err, results) {
    if(err) return cb(err);
    cb(null, results);
  });
}
```
- example usage
```shell
...
   });
 }

 var where = query.criteria.where || {};
 var queryOptions = _.omit(query.criteria, 'where');

 // Run Normal Query on collection
 collection.find(where, query.select, queryOptions).toArray(function(err, docs) {
   if(err) return cb(err);
   cb(null, utils.normalizeResults(docs, self.schema));
 });
};

/**
* Stream Documents
...
```

#### <a name="apidoc.element.sails-mongo.join"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>join (connectionName, collectionName, criteria, cb)](#apidoc.element.sails-mongo.join)
- description and source-code
```javascript
join = function (connectionName, collectionName, criteria, cb) {

  // Ignore 'select' from waterline core
  if (typeof criteria === 'object') {
    delete criteria.select;
  }

  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Populate associated records for each parent result
  // (or do them all at once as an optimization, if possible)
  _runJoins({

    instructions: criteria,
    parentCollection: collectionName,

<span class="apidocCodeCommentSpan">    /**
     * Find some records directly (using only this adapter)
     * from the specified collection.
     *
     * @param  {String}   collectionIdentity
     * @param  {Object}   criteria
     * @param  {Function} cb
     */
</span>    $find: function (collectionIdentity, criteria, cb) {
      var connectionObject = connections[connectionName];
      var collection = connectionObject.collections[collectionIdentity];
      return collection.find(criteria, cb);
    },

    /**
     * Look up the name of the primary key field
     * for the collection with the specified identity.
     *
     * @param  {String}   collectionIdentity
     * @return {String}
     */
    $getPK: function (collectionIdentity) {
      if (!collectionIdentity) return;
      var connectionObject = connections[connectionName];
      if (!connectionObject) {
        throw new Error('Consistency violation in sails-mongo: Unrecognized datastore (i.e. connection): ''+connectionName+''.');
      }
      var collection = connectionObject.collections[collectionIdentity];
      if (!collection) {
        throw new Error('Consistency violation in sails-mongo: Unrecognized collection: ''+collectionIdentity+'' in datastore (i
.e. connection): ''+connectionName+''.');
      }
      return collection._getPK();
    }
  }, cb);

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.native"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>native (connectionName, collectionName, cb)](#apidoc.element.sails-mongo.native)
- description and source-code
```javascript
native = function (connectionName, collectionName, cb) {

  var connectionObject = connections[connectionName];
  cb(null, connectionObject.connection.db.collection(collectionName));

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.registerConnection"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>registerConnection (connection, collections, cb)](#apidoc.element.sails-mongo.registerConnection)
- description and source-code
```javascript
registerConnection = function (connection, collections, cb) {
  if(!connection.identity) return cb(Errors.IdentityMissing);
  if(connections[connection.identity]) return cb(Errors.IdentityDuplicate);

  // Merging default options
  connection = _.defaults(connection, this.defaults);

  // Store the connection
  connections[connection.identity] = {
    config: connection,
    collections: {}
  };

  // Create a new active connection
  new Connection(connection, function(_err, db) {

    if(_err) {
      return cb((function _createError(){
        var msg = util.format('Failed to connect to MongoDB.  Are you sure your configured Mongo instance is running?\n Error details
:\n%s', util.inspect(_err, false, null));
        var err = new Error(msg);
        err.originalError = _err;
        return err;
      })());
    }
    connections[connection.identity].connection = db;

    // Build up a registry of collections
    Object.keys(collections).forEach(function(key) {
      connections[connection.identity].collections[key] = new Collection(collections[key], db);
    });

    cb();
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.stream"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>stream (connectionName, collectionName, options, stream)](#apidoc.element.sails-mongo.stream)
- description and source-code
```javascript
stream = function (connectionName, collectionName, options, stream) {
  options = options || {};
  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  collection.stream(options, stream);
}
```
- example usage
```shell
...

  var collection = this.connection.db.collection(self.identity);

  var where = query.criteria.where || {};
  var queryOptions = _.omit(query.criteria, 'where');

  // Run Normal Query on collection
  var dbStream = collection.find(where, queryOptions).stream();

  // For each data item
  dbStream.on('data', function(item) {
// Pause stream
dbStream.pause();

var obj = utils.rewriteIds([item], self.schema)[0];
...
```

#### <a name="apidoc.element.sails-mongo.teardown"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>teardown (conn, cb)](#apidoc.element.sails-mongo.teardown)
- description and source-code
```javascript
teardown = function (conn, cb) {
  if (typeof conn == 'function') {
    cb = conn;
    conn = null;
  }

  if (conn === null) {
    var _connections = _.pluck(_.values(connections), 'connection');
    if(!_connections.length) { return cb(); }

    var dbs = _.pluck(_connections, 'db');
    if(!dbs.length) { return cb(); }

    connections = {};
    return async.each(dbs, function (db, onClosed) {
      if(db === undefined) { return onClosed(); }
      db.close(onClosed);
    }, cb);
  }

  if(!connections[conn]) return cb();

  var dbConnection = connections[conn].connection.db;
  dbConnection.close(function () {
    delete connections[conn];
    cb();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.update"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>update (connectionName, collectionName, options, values, cb)](#apidoc.element.sails-mongo.update)
- description and source-code
```javascript
update = function (connectionName, collectionName, options, values, cb) {
  options = options || {};
  var connectionObject = connections[connectionName];
  var collection = connectionObject.collections[collectionName];

  // Update matching documents
  collection.update(options, values, function(err, results) {
    if(err) return cb(utils.clarifyError(err));
    cb(null, results);
  });
}
```
- example usage
```shell
...
    var updatedRecords = [];

    records.forEach(function(record) {
updatedRecords.push(record._id);
    });

    // Update the records
    collection.update(query.criteria.where, { '$set': values }, { multi: true }, function(err, result) {
if(err) return cb(err);

// Look up newly inserted records to return the results of the update
collection.find({ _id: { '$in': updatedRecords }}).toArray(function(err, records) {
  if(err) return cb(err);
  cb(null, utils.rewriteIds(records, self.schema));
});
...
```



# <a name="apidoc.module.sails-mongo.collection"></a>[module sails-mongo.collection](#apidoc.module.sails-mongo.collection)

#### <a name="apidoc.element.sails-mongo.collection.collection"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>collection (definition, connection)](#apidoc.element.sails-mongo.collection.collection)
- description and source-code
```javascript
function Collection(definition, connection) {

  // Set an identity for this collection
  this.identity = '';

  // Hold Schema Information
  this.schema = null;

  // Hold a reference to an active connection
  this.connection = connection;

  // Hold the config object
  var connectionConfig = connection.config || {};
  this.config = _.extend({}, connectionConfig.wlNext);

  // Hold Indexes
  this.indexes = [];

  // Parse the definition into collection attributes
  this._parseDefinition(definition);

  // Build an indexes dictionary
  this._buildIndexes();

  return this;
}
```
- example usage
```shell
...
// Catch errors from building query and return to the callback
try {
  query = new Query(criteria, this.schema, this.config);
} catch(err) {
  return cb(err);
}

var collection = this.connection.db.collection(self.identity);

// Check for aggregate query
if(query.aggregate) {
  var aggregate = [
    { '$match': query.criteria.where || {} },
    { '$group': query.aggregateGroup }
  ];
...
```



# <a name="apidoc.module.sails-mongo.collection.prototype"></a>[module sails-mongo.collection.prototype](#apidoc.module.sails-mongo.collection.prototype)

#### <a name="apidoc.element.sails-mongo.collection.prototype._buildIndexes"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>_buildIndexes ()](#apidoc.element.sails-mongo.collection.prototype._buildIndexes)
- description and source-code
```javascript
function _buildIndexes() {
  var self = this;

  Object.keys(this.schema).forEach(function(key) {
    var index = {};
    var options = {};

    // If index key is 'id' ignore it because Mongo will automatically handle this
    if(key === 'id') {
      return;
    }

    // Handle Unique Indexes
    if(self.schema[key].unique) {

      // Set the index sort direction, doesn't matter for single key indexes
      index[key] = 1;

      // Set the index options
      options.sparse = true;
      options.unique = true;

      // Store the index in the collection
      self.indexes.push({ index: index, options: options });
      return;
    }

    // Handle non-unique indexes
    if(self.schema[key].index) {

      // Set the index sort direction, doesn't matter for single key indexes
      index[key] = 1;

      // Set the index options
      options.sparse = true;

      // Store the index in the collection
      self.indexes.push({ index: index, options: options });
      return;
    }
  });
}
```
- example usage
```shell
...
  // Hold Indexes
  this.indexes = [];

  // Parse the definition into collection attributes
  this._parseDefinition(definition);

  // Build an indexes dictionary
  this._buildIndexes();

  return this;
};


/////////////////////////////////////////////////////////////////////////////////
// PUBLIC METHODS
...
```

#### <a name="apidoc.element.sails-mongo.collection.prototype._getPK"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>_getPK ()](#apidoc.element.sails-mongo.collection.prototype._getPK)
- description and source-code
```javascript
function _getPK() {
  var self = this;
  var pk;

  _.keys(this.schema).forEach(function(key) {
    if(self.schema[key].primaryKey) pk = key;
  });

  if(!pk) pk = 'id';
  return pk;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.collection.prototype._parseDefinition"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>_parseDefinition (definition)](#apidoc.element.sails-mongo.collection.prototype._parseDefinition)
- description and source-code
```javascript
function _parseDefinition(definition) {
  var self = this;

  // Hold the Schema
  this.schema = _.cloneDeep(definition.definition);

  if (_.has(this.schema, 'id') && this.schema.id.primaryKey && this.schema.id.type === 'integer') {
    this.schema.id.type = 'objectid';
  }

  // Remove any Auto-Increment Keys, Mongo currently doesn't handle this well without
  // creating additional collection for keeping track of the increment values
  Object.keys(this.schema).forEach(function(key) {
    if(self.schema[key].autoIncrement) delete self.schema[key].autoIncrement;
  });

  // Replace any foreign key value types with ObjectId
  Object.keys(this.schema).forEach(function(key) {
    if(self.schema[key].foreignKey) {
      self.schema[key].type = 'objectid';
    }
  });

  // Set the identity
	var ident = definition.tableName ? definition.tableName : definition.identity.toLowerCase();
	this.identity = _.clone(ident);
}
```
- example usage
```shell
...
  var connectionConfig = connection.config || {};
  this.config = _.extend({}, connectionConfig.wlNext);

  // Hold Indexes
  this.indexes = [];

  // Parse the definition into collection attributes
  this._parseDefinition(definition);

  // Build an indexes dictionary
  this._buildIndexes();

  return this;
};
...
```

#### <a name="apidoc.element.sails-mongo.collection.prototype.count"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>count (criteria, cb)](#apidoc.element.sails-mongo.collection.prototype.count)
- description and source-code
```javascript
function count(criteria, cb) {

  var self = this;
  var query;

  // Ignore 'select' from waterline core
  if (typeof criteria === 'object') {
    delete criteria.select;
  }

  // Catch errors build query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return cb(err);
  }

  this.connection.db.collection(this.identity).count(query.criteria.where, function(err, count) {
    if (err) return cb(err);
    cb(null, count);
  });
}
```
- example usage
```shell
...
  // Catch errors build query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return cb(err);
  }

  this.connection.db.collection(this.identity).count(query.criteria.where, function(err, count) {
    if (err) return cb(err);
    cb(null, count);
  });
};


/////////////////////////////////////////////////////////////////////////////////
...
```

#### <a name="apidoc.element.sails-mongo.collection.prototype.destroy"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>destroy (criteria, cb)](#apidoc.element.sails-mongo.collection.prototype.destroy)
- description and source-code
```javascript
function destroy(criteria, cb) {
  var self = this,
      query;

  // Ignore 'select' from waterline core
  if (typeof criteria === 'object') {
    delete criteria.select;
  }

  // Catch errors build query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return cb(err);
  }

  var collection = this.connection.db.collection(self.identity);
  collection.remove(query.criteria.where, function(err, results) {
    if(err) return cb(err);

    // Force to array to meet Waterline API
    var resultsArray = [];

    // If result is not an array return an array
    if(!Array.isArray(results)) {
      resultsArray.push({ id: results });
      return cb(null, resultsArray);
    }

    // Create a valid array of IDs
    results.forEach(function(result) {
      resultsArray.push({ id: result });
    });

    cb(null, utils.rewriteIds(resultArray, self.schema));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.collection.prototype.find"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>find (criteria, cb)](#apidoc.element.sails-mongo.collection.prototype.find)
- description and source-code
```javascript
function find(criteria, cb) {
  var self = this,
      query;

  // Catch errors from building query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return cb(err);
  }

  var collection = this.connection.db.collection(self.identity);

  // Check for aggregate query
  if(query.aggregate) {
    var aggregate = [
      { '$match': query.criteria.where || {} },
      { '$group': query.aggregateGroup }
    ];

    return collection.aggregate(aggregate, function(err, results) {

      // Results have grouped by values under _id, so we extract them
      var mapped = results.map(function(result) {
        for(var key in result._id) {
          result[key] = result._id[key];
        }
        delete result._id;
        return result;
      });

      cb(err, mapped);
    });
  }

  var where = query.criteria.where || {};
  var queryOptions = _.omit(query.criteria, 'where');

  // Run Normal Query on collection
  collection.find(where, query.select, queryOptions).toArray(function(err, docs) {
    if(err) return cb(err);
    cb(null, utils.normalizeResults(docs, self.schema));
  });
}
```
- example usage
```shell
...
   });
 }

 var where = query.criteria.where || {};
 var queryOptions = _.omit(query.criteria, 'where');

 // Run Normal Query on collection
 collection.find(where, query.select, queryOptions).toArray(function(err, docs) {
   if(err) return cb(err);
   cb(null, utils.normalizeResults(docs, self.schema));
 });
};

/**
* Stream Documents
...
```

#### <a name="apidoc.element.sails-mongo.collection.prototype.insert"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>insert (values, cb)](#apidoc.element.sails-mongo.collection.prototype.insert)
- description and source-code
```javascript
function insert(values, cb) {

  var self = this;

  // Normalize values to an array
  if(!Array.isArray(values)) values = [values];

  // Build a Document and add the values to a new array
  var docs = values.map(function(value) {
    return new Document(value, self.schema).values;
  });

  this.connection.db.collection(this.identity).insert(docs, function(err, results) {
    if(err) return cb(err);
    cb(null, utils.rewriteIds(results.ops, self.schema));
  });
}
```
- example usage
```shell
...
 if(!Array.isArray(values)) values = [values];

 // Build a Document and add the values to a new array
 var docs = values.map(function(value) {
   return new Document(value, self.schema).values;
 });

 this.connection.db.collection(this.identity).insert(docs, function(err, results) {
   if(err) return cb(err);
   cb(null, utils.rewriteIds(results.ops, self.schema));
 });
};

/**
* Update Documents
...
```

#### <a name="apidoc.element.sails-mongo.collection.prototype.stream"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>stream (criteria, stream)](#apidoc.element.sails-mongo.collection.prototype.stream)
- description and source-code
```javascript
function find(criteria, stream) {
  var self = this,
    query;

  // Ignore 'select' from waterline core
  if (typeof criteria === 'object') {
    delete criteria.select;
  }

  // Catch errors from building query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return stream.end(err); // End stream
  }

  var collection = this.connection.db.collection(self.identity);

  var where = query.criteria.where || {};
  var queryOptions = _.omit(query.criteria, 'where');

  // Run Normal Query on collection
  var dbStream = collection.find(where, queryOptions).stream();

  // For each data item
  dbStream.on('data', function(item) {
    // Pause stream
    dbStream.pause();

    var obj = utils.rewriteIds([item], self.schema)[0];

    stream.write(obj, function() {
      dbStream.resume();
    });

  });

  // Handle error, an 'end' event will be emitted after this as well
  dbStream.on('error', function(err) {
    stream.end(err); // End stream
  });

  // all rows have been received
  dbStream.on('close', function() {
    stream.end();
  });
  // stream has ended
  dbStream.on('end', function() {
    stream.end();
  });
}
```
- example usage
```shell
...

  var collection = this.connection.db.collection(self.identity);

  var where = query.criteria.where || {};
  var queryOptions = _.omit(query.criteria, 'where');

  // Run Normal Query on collection
  var dbStream = collection.find(where, queryOptions).stream();

  // For each data item
  dbStream.on('data', function(item) {
// Pause stream
dbStream.pause();

var obj = utils.rewriteIds([item], self.schema)[0];
...
```

#### <a name="apidoc.element.sails-mongo.collection.prototype.update"></a>[function <span class="apidocSignatureSpan">sails-mongo.collection.prototype.</span>update (criteria, values, cb)](#apidoc.element.sails-mongo.collection.prototype.update)
- description and source-code
```javascript
function update(criteria, values, cb) {
  var self = this,
      query;

  // Ignore 'select' from waterline core
  if (typeof criteria === 'object') {
    delete criteria.select;
  }

  // Catch errors build query and return to the callback
  try {
    query = new Query(criteria, this.schema, this.config);
  } catch(err) {
    return cb(err);
  }

  values = new Document(values, this.schema).values;

  // Mongo doesn't allow ID's to be updated
  if(values.id) delete values.id;
  if(values._id) delete values._id;

  var collection = this.connection.db.collection(self.identity);

  // Lookup records being updated and grab their ID's
  // Useful for later looking up the record after an insert
  // Required because options may not contain an ID
  collection.find(query.criteria.where, {_id: 1}).toArray(function(err, records) {
    if(err) return cb(err);
    if(!records) return cb(Errors.NotFound);

    // Build an array of records
    var updatedRecords = [];

    records.forEach(function(record) {
      updatedRecords.push(record._id);
    });

    // Update the records
    collection.update(query.criteria.where, { '$set': values }, { multi: true }, function(err, result) {
      if(err) return cb(err);

      // Look up newly inserted records to return the results of the update
      collection.find({ _id: { '$in': updatedRecords }}).toArray(function(err, records) {
        if(err) return cb(err);
        cb(null, utils.rewriteIds(records, self.schema));
      });
    });
  });
}
```
- example usage
```shell
...
    var updatedRecords = [];

    records.forEach(function(record) {
updatedRecords.push(record._id);
    });

    // Update the records
    collection.update(query.criteria.where, { '$set': values }, { multi: true }, function(err, result) {
if(err) return cb(err);

// Look up newly inserted records to return the results of the update
collection.find({ _id: { '$in': updatedRecords }}).toArray(function(err, records) {
  if(err) return cb(err);
  cb(null, utils.rewriteIds(records, self.schema));
});
...
```



# <a name="apidoc.module.sails-mongo.connection"></a>[module sails-mongo.connection](#apidoc.module.sails-mongo.connection)

#### <a name="apidoc.element.sails-mongo.connection.connection"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>connection (config, cb)](#apidoc.element.sails-mongo.connection.connection)
- description and source-code
```javascript
function Connection(config, cb) {
  var self = this;

  // Hold the config object
  this.config = config || {};

  // Build Database connection
  this._buildConnection(function(err, db) {
    if(err) return cb(err);
    if(!db) return cb(new Error('no db object'));

    // Store the DB object
    self.db = db;

    // Return the connection
    cb(null, self);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sails-mongo.connection.prototype"></a>[module sails-mongo.connection.prototype](#apidoc.module.sails-mongo.connection.prototype)

#### <a name="apidoc.element.sails-mongo.connection.prototype._buildConnection"></a>[function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>_buildConnection (cb)](#apidoc.element.sails-mongo.connection.prototype._buildConnection)
- description and source-code
```javascript
function _buildConnection(cb) {

  // Set the configured options
  var connectionOptions = {};

  connectionOptions.mongos = this.config.mongos || {};
  connectionOptions.replSet = this.config.replSet || {};

  // Build up options used for creating a Server instance
  connectionOptions.server = {
    readPreference: this.config.readPreference,
    ssl: this.config.ssl,
    sslValidate: this.config.sslValidate,
    sslCA: this.config.sslCA,
    sslCert: this.config.sslCert,
    sslKey: this.config.sslKey,
    poolSize: this.config.poolSize,
    socketOptions: this.config.socketOptions,
    autoReconnect: this.config.auto_reconnect,
    disableDriverBSONSizeCheck: this.config.disableDriverBSONSizeCheck,
    reconnectInterval: this.config.reconnectInterval,
    reconnectTries: this.config.reconnectTries
  };

  // Build up options used for creating a Database instance
  connectionOptions.db = {
    w: this.config.w,
    wtimeout: this.config.wtimeout,
    fsync: this.config.fsync,
    journal: this.config.journal,
    readPreference: this.config.readPreference,
    native_parser: this.config.nativeParser,
    forceServerObjectId: this.config.forceServerObjectId,
    recordQueryStats: this.config.recordQueryStats,
    retryMiliSeconds: this.config.retryMiliSeconds,
    numberOfRetries: this.config.numberOfRetries
  };

  // Support for encoded auth credentials
  connectionOptions.uri_decode_auth = this.config.uri_decode_auth || false;

  // Build A Mongo Connection String
  var connectionString = 'mongodb://';

  // If auth is used, append it to the connection string
  if(this.config.user && this.config.password) {

    // Ensure a database was set if auth in enabled
    if(!this.config.database) {
      throw new Error('The MongoDB Adapter requires a database config option if authentication is used.');
    }

    connectionString += this.config.user + ':' + this.config.password + '@';
  }

  // Append the host and port
  connectionString += this.config.host + ':' + this.config.port + '/';

  if(this.config.database) {
    connectionString += this.config.database;
  }

  // Use config connection string if available
  if(this.config.url) connectionString = this.config.url;

  // Open a Connection
  MongoClient.connect(connectionString, connectionOptions, cb);
}
```
- example usage
```shell
...
var Connection = module.exports = function Connection(config, cb) {
  var self = this;

  // Hold the config object
  this.config = config || {};

  // Build Database connection
  this._buildConnection(function(err, db) {
if(err) return cb(err);
if(!db) return cb(new Error('no db object'));

// Store the DB object
self.db = db;

// Return the connection
...
```

#### <a name="apidoc.element.sails-mongo.connection.prototype._ensureIndexes"></a>[function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>_ensureIndexes (collection, indexes, cb)](#apidoc.element.sails-mongo.connection.prototype._ensureIndexes)
- description and source-code
```javascript
function _ensureIndexes(collection, indexes, cb) {
  var self = this;

  function createIndex(item, next) {
    collection.ensureIndex(item.index, item.options, next);
  }

  async.each(indexes, createIndex, cb);
}
```
- example usage
```shell
...
 var self = this;

 // Create the Collection
 this.db.createCollection(name, function(err, result) {
   if(err) return cb(err);

   // Create Indexes
   self._ensureIndexes(result, collection.indexes, cb);
 });
};

/**
* Drop A Collection
*
* @param {String} name
...
```

#### <a name="apidoc.element.sails-mongo.connection.prototype.createCollection"></a>[function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>createCollection (name, collection, cb)](#apidoc.element.sails-mongo.connection.prototype.createCollection)
- description and source-code
```javascript
function createCollection(name, collection, cb) {
  var self = this;

  // Create the Collection
  this.db.createCollection(name, function(err, result) {
    if(err) return cb(err);

    // Create Indexes
    self._ensureIndexes(result, collection.indexes, cb);
  });
}
```
- example usage
```shell
...
 * @api public
 */

Connection.prototype.createCollection = function createCollection(name, collection, cb) {
  var self = this;

  // Create the Collection
  this.db.createCollection(name, function(err, result) {
    if(err) return cb(err);

    // Create Indexes
    self._ensureIndexes(result, collection.indexes, cb);
  });
};
...
```

#### <a name="apidoc.element.sails-mongo.connection.prototype.dropCollection"></a>[function <span class="apidocSignatureSpan">sails-mongo.connection.prototype.</span>dropCollection (name, cb)](#apidoc.element.sails-mongo.connection.prototype.dropCollection)
- description and source-code
```javascript
function dropCollection(name, cb) {
  this.db.dropCollection(name, cb);
}
```
- example usage
```shell
...
 *
 * @param {String} name
 * @param {Function} callback
 * @api public
 */

Connection.prototype.dropCollection = function dropCollection(name, cb) {
  this.db.dropCollection(name, cb);
};


/////////////////////////////////////////////////////////////////////////////////
// PRIVATE METHODS
/////////////////////////////////////////////////////////////////////////////////
...
```



# <a name="apidoc.module.sails-mongo.document"></a>[module sails-mongo.document](#apidoc.module.sails-mongo.document)

#### <a name="apidoc.element.sails-mongo.document.document"></a>[function <span class="apidocSignatureSpan">sails-mongo.</span>document (values, schema)](#apidoc.element.sails-mongo.document.document)
- description and source-code
```javascript
function Document(values, schema) {

  // Keep track of the current document's values
  this.values = {};

  // Grab the schema for normalizing values
  this.schema = schema || {};

  // If values were passed in, use the setter
  if(values) this.values = this.setValues(values);

  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sails-mongo.document.prototype"></a>[module sails-mongo.document.prototype](#apidoc.module.sails-mongo.document.prototype)

#### <a name="apidoc.element.sails-mongo.document.prototype.normalizeId"></a>[function <span class="apidocSignatureSpan">sails-mongo.document.prototype.</span>normalizeId (values)](#apidoc.element.sails-mongo.document.prototype.normalizeId)
- description and source-code
```javascript
function normalizeId(values) {

  if(!values.id) return;

  // Check if data.id looks like a MongoID
  if(_.isString(values.id) && values.id.match(/^[a-fA-F0-9]{24}$/)) {

    values._id = new ObjectId.createFromHexString(values.id);
  } else {

    values._id = _.cloneDeep(values.id);
  }

  delete values.id;
}
```
- example usage
```shell
...
* @param {Object} values
* @return {Object}
* @api private
*/

Document.prototype.setValues = function setValues(values) {
 this.serializeValues(values);
 this.normalizeId(values);

 return values;
};

/**
* Normalize ID's
*
...
```

#### <a name="apidoc.element.sails-mongo.document.prototype.serializeValues"></a>[function <span class="apidocSignatureSpan">sails-mongo.document.prototype.</span>serializeValues (values)](#apidoc.element.sails-mongo.document.prototype.serializeValues)
- description and source-code
```javascript
function serializeValues(values) {
  var self = this;

  Object.keys(values).forEach(function(key) {
    if(!hasOwnProperty(self.schema, key)) return;

    var type = self.schema[key].type,
        val;

    var foreignKey = self.schema[key].foreignKey || false;

    if(_.isUndefined(values[key])) return;

    // If a foreignKey, check if value matches a mongo id and if so turn it into an objectId
    if(foreignKey && utils.matchMongoId(values[key])) {
      values[key] = new ObjectId.createFromHexString(values[key]);
    }

    if(type === 'json') {
      try {
        val = JSON.parse(values[key]);
      } catch(e) {
        return;
      }
      values[key] = val;
    }
  });

  return values;
}
```
- example usage
```shell
...
*
* @param {Object} values
* @return {Object}
* @api private
*/

Document.prototype.setValues = function setValues(values) {
 this.serializeValues(values);
 this.normalizeId(values);

 return values;
};

/**
* Normalize ID's
...
```

#### <a name="apidoc.element.sails-mongo.document.prototype.setValues"></a>[function <span class="apidocSignatureSpan">sails-mongo.document.prototype.</span>setValues (values)](#apidoc.element.sails-mongo.document.prototype.setValues)
- description and source-code
```javascript
function setValues(values) {
  this.serializeValues(values);
  this.normalizeId(values);

  return values;
}
```
- example usage
```shell
...
  // Keep track of the current document's values
  this.values = {};

  // Grab the schema for normalizing values
  this.schema = schema || {};

  // If values were passed in, use the setter
  if(values) this.values = this.setValues(values);

  return this;
};


/////////////////////////////////////////////////////////////////////////////////
// PRIVATE METHODS
...
```



# <a name="apidoc.module.sails-mongo.mongo"></a>[module sails-mongo.mongo](#apidoc.module.sails-mongo.mongo)

#### <a name="apidoc.element.sails-mongo.mongo.objectId"></a>[function <span class="apidocSignatureSpan">sails-mongo.mongo.</span>objectId (id)](#apidoc.element.sails-mongo.mongo.objectId)
- description and source-code
```javascript
objectId = function (id){
  if(!id) return null;
  try {
    return new ObjectId(id);
  } catch(err) {
    return null;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sails-mongo.utils"></a>[module sails-mongo.utils](#apidoc.module.sails-mongo.utils)

#### <a name="apidoc.element.sails-mongo.utils._rewriteIds"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>_rewriteIds (model, schema)](#apidoc.element.sails-mongo.utils._rewriteIds)
- description and source-code
```javascript
_rewriteIds = function (model, schema) {
  if (hop.call(model, '_id')) {
    // change id to string only if it's necessary
    if (typeof model._id === 'object' && model._id._bsontype)
      model.id = model._id.toString();
    else
      model.id = model._id;
    delete model._id;
  }

  // Rewrite any foreign keys if a schema is available
  if (!schema) return model;

  Object.keys(schema).forEach(function (key) {
    var foreignKey = schema[key].foreignKey || false;

    // If a foreignKey, check if value matches a mongo id and if so turn it into an objectId
    if (foreignKey && model[key] instanceof ObjectId) {
      model[key] = model[key].toString();
    }
  });

  return model;
}
```
- example usage
```shell
...
*
* @param {Array} models
* @api public
*/

exports.rewriteIds = function rewriteIds(models, schema) {
 var _models = models.map(function(model){
   return exports._rewriteIds(model, schema);
 });
 return _models;
};

/**
* Normalize documents retrieved from MongoDB to match Waterline's expectations
*
...
```

#### <a name="apidoc.element.sails-mongo.utils.caseInsensitive"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>caseInsensitive (val)](#apidoc.element.sails-mongo.utils.caseInsensitive)
- description and source-code
```javascript
function caseInsensitive(val) {
  if(!_.isString(val)) return val;
  return val.replace(/[-[\]{}()+?*.\/,\\^$|#]/g, "\\$&");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.utils.clarifyError"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>clarifyError (err)](#apidoc.element.sails-mongo.utils.clarifyError)
- description and source-code
```javascript
function clarifyError(err) {
  // MongoDB duplicate key error code
  if(err.code !== 11000) {
    return err;
  }

  // Example errmsg: 'E11000 duplicate key error index: db_name.model_name.$attribute_name_1 dup key: { : "value" }'
  var matches = /E11000 duplicate key error index: .*?\..*?\.\$(.*?)_\d+\s+dup key: { : (.*) }$/.exec(err.errmsg);
  if (!matches) {
    // Example errmsg: E11000 duplicate key error collection: db_name.model_name index: attribute_name_1 dup key: { : "value" }
    matches = /E11000 duplicate key error collection: .*?\..*? index: (.*?)_\d+\s+dup key: { : (.*) }$/.exec(err.errmsg);
    if (!matches) {
      // We cannot parse error message, return original error
      return err;
    }
  }
  var fieldName = matches[1]; // name of index (without _[digits] at the end)
  var value;
  try {
    value = JSON.parse(matches[2]); // attempt to convert the value to a primitive representation
  } catch (x) {
    value = matches[2]; // for non-serializable objects (e.g. ObjectId representations), return as-is
  }

  var validationError = {
    code: 'E_UNIQUE',
    invalidAttributes: {},
    originalError: err
  };

  validationError.invalidAttributes[fieldName] = [
    {
      rule: 'unique',
      value: value
    }
  ];

  return validationError;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.utils.matchMongoId"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>matchMongoId (id)](#apidoc.element.sails-mongo.utils.matchMongoId)
- description and source-code
```javascript
function matchMongoId(id) {
  if (id === null) return false;
  var test = _.cloneDeep(id);
  if(typeof test.toString !== 'undefined') test = id.toString();
  return test.match(/^[a-fA-F0-9]{24}$/) ? true : false;
}
```
- example usage
```shell
...
    val;

var foreignKey = self.schema[key].foreignKey || false;

if(_.isUndefined(values[key])) return;

// If a foreignKey, check if value matches a mongo id and if so turn it into an objectId
if(foreignKey && utils.matchMongoId(values[key])) {
  values[key] = new ObjectId.createFromHexString(values[key]);
}

if(type === 'json') {
  try {
    val = JSON.parse(values[key]);
  } catch(e) {
...
```

#### <a name="apidoc.element.sails-mongo.utils.normalizeResults"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>normalizeResults (models, schema)](#apidoc.element.sails-mongo.utils.normalizeResults)
- description and source-code
```javascript
function normalizeResults(models, schema) {
  var _models = models.map(function (model) {
    var _model = exports._rewriteIds(model, schema);
    Object.keys(_model).forEach(function (key) {
      if (model[key] instanceof MongoBinary && _.has(_model[key], 'buffer')) {
        _model[key] = _model[key].buffer;
      }
    });
    return _model;
  });
  return _models;
}
```
- example usage
```shell
...

 var where = query.criteria.where || {};
 var queryOptions = _.omit(query.criteria, 'where');

 // Run Normal Query on collection
 collection.find(where, query.select, queryOptions).toArray(function(err, docs) {
   if(err) return cb(err);
   cb(null, utils.normalizeResults(docs, self.schema));
 });
};

/**
* Stream Documents
*
* @param {Object} criteria
...
```

#### <a name="apidoc.element.sails-mongo.utils.parseUrl"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>parseUrl (config)](#apidoc.element.sails-mongo.utils.parseUrl)
- description and source-code
```javascript
function parseUrl(config) {
  if(!_.isString(config.url)) return config;

  var obj = url.parse(config.url);

  config.host = obj.hostname || config.host;
  config.port = obj.port || config.port;

  if(_.isString(obj.path)) {
    config.database = obj.path.split("/")[1] || config.database;
  }

  if(_.isString(obj.auth)) {
    config.user = obj.auth.split(":")[0] || config.user;
    config.password = obj.auth.split(":")[1] || config.password;
  }

  return config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sails-mongo.utils.rewriteIds"></a>[function <span class="apidocSignatureSpan">sails-mongo.utils.</span>rewriteIds (models, schema)](#apidoc.element.sails-mongo.utils.rewriteIds)
- description and source-code
```javascript
function rewriteIds(models, schema) {
  var _models = models.map(function(model){
    return exports._rewriteIds(model, schema);
  });
  return _models;
}
```
- example usage
```shell
...
var dbStream = collection.find(where, queryOptions).stream();

// For each data item
dbStream.on('data', function(item) {
  // Pause stream
  dbStream.pause();

  var obj = utils.rewriteIds([item], self.schema)[0];

  stream.write(obj, function() {
    dbStream.resume();
  });

});
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
