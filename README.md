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

test.open('http://doctorwhotv.co.uk')
  .assert.chain()
    .query('#nav')
      .text().is('Navigation')
      .visible()
      .attr('data-nav', 'true')
    .end()
  .end()
  .done();
  
test.open('httpL..doctorwhotv.co.uk/')
  .assert.chain()
    .query('#nav')
      .text().is('Nabigation')
      .visible()
      .attr('data-nav', 'true')
    .end()
  .end()
  .done();
  
test.assert.numberOfElement();

test.assert.numberOfElement('#blog-overview .teaser')
  .is(4, '4 blog teasers are present')
```

```
```

```
```


