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
var anonym = {
 idb: function() {
  //check for support
  if (!('indexedDB' in window)) {
    console.log('This browser doesn\'t support IndexedDB');
  }
  else {return idb = window.indexedDB}

  var request = idb.open("MyTestDatabase", 3);
      var promiseObj = new Promise((resolve, reject) =>{
      if (request) {
      resolve(event);
      } else {
      reject(event)
      }
      });
      promiseObj.then((event)=> {idb = event.target.result;
      idb.databases();
      });
      promiseObj.catch((event)=> {console.log("Why didn't you allow my web app to use IndexedDB?!")})}};
anonym.idb();
```
