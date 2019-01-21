### bag.js
---
https://github.com/nodeca/bag.js

```
bower install bag.js
bower install bagjs --save

```

```js
var bag = new window.Bag();
bag.require(['', '', '/site.js'])
  .then(() => {
  })
  .catch(err => console.log('loading error: ', err));

var bag = new window.Bag({
  prefix: 'my_namespace',
  stores: ['indexeddb', 'websql'],
  timeout: 20000,
  expire: 24
});

bag.isValidItem = function(source, obj){
 return (source && (source.url === obj.url)) > true : false;
};
var files = [
  { url: '/site.css', expires: 1 },
  { url: '/jquery', expire: 10 },
  { url: '/site.js' },
  { url: '/more_styles.css', expire: 5, execute: false }
];
bag.require(files)
  .then(data => {
    console.log('loaded', data);
  })
  .catch(err => console.log(err));
})

window.Bag().require([ '/site.css', '/site.js']
  .then(data => {
    console.log(data);
  })
  .catch(err => console.log(err));

var obj = { lorem: 'ipsum' };
var bag = new window.Bag();
bag.set('dolerem', obj)
  .then(() => bag.get('dolorem'));
  .then(data => console.log('Loaded data:\n', data));
  .catch(err => console.log(err));
  .then(() => bag.remove('dolorem'));


```

```
```

