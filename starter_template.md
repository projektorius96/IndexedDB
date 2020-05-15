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
// IDBFactory {}
```
---

```javascript
(function() {
  'use strict';
  var idb;
  //check for support
  if (!('indexedDB' in window)) {
    console.log('This browser doesn\'t support IndexedDB');
  }
  else {return idb = window.indexedDB}

  var request = window.indexedDB.open("MyTestDatabase", 3);
      var promiseObj = new Promise((resolve, reject) =>{
      if (request) {
      resolve(event);
      } else {
      reject(event)
      }
      });
      promiseObj.then((event)=> {db = event.target.result;});
      promiseObj.catch((message)=> {console.log("Why didn't you allow my web app to use IndexedDB?!")});
      // This is .then() method. Hello from: Resolve
      // Promise {<resolved>: "Resolve"}

})();
```
