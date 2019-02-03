### dalek
---
https://github.com/dalekjs/dalek

```js
test.open()
  .assert.text().is()
  .assert.visible()
  .assert.attr()
  .done();
  
test.open('http://doctorwhotv.co.uk')
  .assert.chain()
    .text('#nav').is('Navigation')
    .visible('#nav')
    .attr('#nav', 'data-nav', 'true')
  .end()
  .done();
```

```
```

```
```


