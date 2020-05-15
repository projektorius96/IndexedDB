[all credits to google devs](https://developers.google.com/web/ilt/pwa/working-with-indexeddb)
```javascript
(function() {
  'use strict';
  var idb;
  //check for support
  if (!('indexedDB' in window)) {
    console.log('This browser doesn\'t support IndexedDB');
  }

  else {return idb = window.indexedDB}

  var dbPromise = idb.open('test-db1', 1);

})();
```
