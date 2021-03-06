# 0.4.3+1

- Downgrade `meta` dependency to `^1.1.6` according to [this](https://github.com/YevhenKap/couchdb_dart/issues/7) issue.

## 0.4.3

- Change signature of `CouchDbClient` to provide `origin` parameter.
- Small fix of docs.

## 0.4.2

- Fix `secret` encoding for non-proxy authentication.
- Make most fields in `CouchDbClient` final.
- Add `shards()`, `shard()` and `synchronizeShards()` methods to `DatabaseModel` class.
- Fix `Origin` construction.

## 0.4.1

- Add `secret` fiels to `CouchDbClient` class for proxy authentication.
- Edit README.

## 0.4.0

- Add cookie authentication.
- Add proxy authentication.
- Add `authenticate()`, `logout()` and `userInfo()` methods to `CouchDbClient` class.
- Add related to authentication fields to `ServerModelResponse` class.

## 0.3.0

- Unit `CouchDbWebClient` and `CouchDbServerClient` to `CouchDbClient` class.
- Add `streamed()` method to `CouchDbClient` class.
- Change `DatabaseModel.changesIn()` and `DatabaseModel.postChangesIn()` methods to return stream of event responses (fix for alive connection).
- Makes all fields of `...Response` classes final.

## 0.2.1

- Fix cast `revsDiff` property in `DbResponse` class.

## 0.2.0

- Split `DbResponse` to five classes corresponds to categories of CouchDB:

        1. Server
        2. Database
        3. Documents
        4. Design documents
        5. Local documents

- Change signatures of some methods (check your code for error and reference to Docs).
- Add `purgedInfosLimit()` and `setPurgedInfosLimit()` to `DatabaseModel` class.
- Improve docs in API docs (add return's JSON example).
- Move `headers` to separate field in `DbResponse` from json.
- Improved README.

## 0.1.4+1

- Downgrade required Dart SDK to `2.1.0-dev.9.4`.

## 0.1.4

- Move `cors` field to `CouchDbWebClient` class.
- Remove `cors` parameter from constructor of `CouchDbServerClient` and `CouchDbBaseClient` classes.

## 0.1.3

- Add `_headers` field, `headers` getter and improve `modifyRequestHeaders()` method of `CouchDbBaseClient` class.
- Move fields and getters from `CouchDb(Server/Web)Client` to `CouchDbBaseClient`.
- Remove `_client` from `CouchDb(Server/Web)Client` and change constructors from being `factory` to usual.
- Add `cors` field to `CouchDbBaseClient` class and its constructor.

## 0.1.2

- Improve README.
- Rename `getAllDocs()` to `allDocs()`, `getAllDesignDocs()` to `allDesignDocs()`,
  `getBulkDocs()` to `bulkDocs()`, `getDocsByKeys()` to `docsByKeys()` methods of `DatabaseModel` class.
- Rename `getDesignDoc()` to `designDoc()`, `getAttachment()` to `attachment()` methods
  of `DesignDocumentModel` class.
- Rename `getDoc()` to `doc()`, `getAttachment()` to `attachment()` methods of `DocumentModel` class.
- Rename `getLocalDocs()` to `localDocs()`, `getLocalDocsWithKeys()` to `localDocsWithKeys()`,
  `getLocalDoc()` to `localDoc()` methods of `LocalDocumentModel` class.
- Rename `getClusterSetup()` to `clusterSetupStatus()` method of `ServerModel` class.
- Add `includeDocs` parameter to `allDocs()` method of `DatabaseModel` class.

## 0.1.1

- Small changes that don't touch main classes.

## 0.1.0

- Introducing beta-version of library.
- Implement all methods of `ServerModel` class.
- Implement all methods of `DesignDocumentModel` class.
- Add library description to `CouchDb(Server/Web)Client` classes.
- Add `raw` field to `DbResponse` class (prior `rawBody`).
- Change `body` parameter of `post()` method in `CouchDb(Server/Web)Client` to `Object` type.

## 0.0.8

- Implements `schedulerJobs()`, `schedulerDocs()`, `schedulerDocsWithReplicatorDbName()`, `schedulerDocsWithDocId()`,
  `nodeStats()`, `systemStatsForNode()`, `up()` and `uuids()` methods of `ServerModel` class.
- Add some fields to `DbResponse` class.

## 0.0.7

- Change `toString()` method of `CouchDbException` class - it shows error code, name error and reason.
- Add `allNodes`, `clusterNodes`, `history`, `replicationIdVersion`, `sessionId` and `sourceLastSeq` fields to `DbResponse` class.
- Implements `configureCouchDb()`, `dbUpdates()`, `membership()` and `replicate()` methods of `ServerModel` class.

## 0.0.6

- Moving `CouchDbWebClient` and `CouchDbServerClient` to the separate export.
- Delete `rawBody` field from `DbResponse` class.
- Add `state` field to `DbResponse` class.
- Implements `couchDbInfo()`, `activeTasks()`, `allDbs()`, `dbsInfo()` and `getClusterSetup()` methods of `ServerModel` class.
- Small changes in `CouchDb(Server/Web)Client` classes.

## 0.0.5

- Implement `CouchDbWebClient` class for interacting with CouchDB.
- Moving all examples to `example/README.md`.

## 0.0.4

- Implements `attachmentInfo()`, `getAttachment()`, `insertAttachment()` and `deleteAttachment()` methods of `DocumentModel` class.
- Implement `setRevsLimit()` method of `DatabaseModel` class.
- Method `put()` now accept any body type.
- Non-json response body now available in `rawBody` field of `DbRespone` class.

## 0.0.3

- Implements `insertDoc()`, `deleteDoc()` and `copyDoc()` methods of `DocumentModel` class.
- All methods of `CouchDb(Server/Web)Client` can set custom headers.

## 0.0.2

- Implementats `docInfo()` and `getDoc()` methods of `DocumentModel` class.
- Add documentation to `DatabaseModel` methods.
- Add opportunity to add headers to `head()` method of `CouchDb(Server/Web)Client` classes.

## 0.0.1

- Initial version.
- Implement `CouchDbServerClient` for interacting with CouchDB.
- Implements `DatabaseBaseModel` methods.