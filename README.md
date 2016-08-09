| Type        | Sync | Async               | Web Workers | Window | Service Workers | Gotchas                                                                                                           | Libraries             |
|-------------|------|---------------------|-------------|--------|-----------------|-------------------------------------------------------------------------------------------------------------------|-----------------------|
| Cookies     | ✔    |                     |             |        |                 | Size-limited, only strings.  Not hooked up to Quota Manager                                                       | js-cookie Cookies.js  |
| DOM Storage | ✔    |                     |             |        |                 | Size-limited, only strings.  Not hooked up to Quota Manager                                                       |                       |
| IndexedDB   |      | ✔  (event based)    | ✔           | ✔      | ✔               | Mandatory complexity  (schema versioning, transactions)                                                           | localForage dexie idb |
| WebSQL      |      | ✔  (callback based) |             |        |                 | Rejected by Edge, Firefox.  Likely to unship in Chrome.                                                           |                       |
| AppCache    |      |                     |             |        |                 | Chrome: Deprecating HTTP support Firefox: Intent to Deprecate                                                     |                       |
| Cache API   |      |  ✔  (promise based) | ✔           | ✔      |                 |                                                                                                                   | sw-toolbox            |
| FileSystem  | ✔    | ✔  (callback based) | ✔           | ✔      |                 | Sandboxed - not native file access No interest from other vendors outside Chrome  (newer Moz proposal abandoned?) |                       |
| File API    |      |                     |             |        |                 | Directory Upload - MSFT and Moz (?)  shipping webkit-prefixed API                                                 |                       |
