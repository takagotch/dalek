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
  
test.assert.numberOfElement('#blog-overview .teaser', 4, '4 blog teasers are present');

test.assert.numberOfElement('#blog-overview .teaser')
  .is(4, '4 blog teasers are present')
  
test
  .assert.val('#the-doctors', 10, 'David is the favourite')
  .click('#the-doctors option:last')
  .assert.val('#the-doctors', 11, 'Matt is now my favourite, bow ties are cool')

test
  .open('http://unicorns.rainbows.io')
  .assert.css('#superColoredElement', 'background-color', 'rgba(255, 0, 0, 1)')
  .assert.css('#superColoredElement', 'color', 'rgba(0, 128, 0, 1)')
  .done();
  
test
  .open('http://unicorns.rainbows.io')
  .assert.css('#fancyPlacedElement', '', '>50px')
  .assert.css('#fancyPlacedElement', 'top', '<150px')
  .assert.css('#fancyPlacedElement', 'top', '>150px')
  .assert.css('#fancyPlacedElement', 'top', '<50px')
  .done();
  
test
  .open('http://localhost:5000/index.html')
  .assert.width('#fixed-dimensions', 100)
  .assert.width('#fixed-dimensions').is(100)
  .assert.width('#fixed-dimensions').is.lte(110)
  .assert.width('#fixed-dimensions').is.between([90, 110])
  .done();
  
test
  .open('http://doctor.thedoctor.com/doctor')
  .assert.doesntExist('#the-master', 'The master elemnet has not been seen')
  .done();
```

```css
#superColoredElement {
  background-color: rgba(255, 0, 0, 1);
  color: rgba(0, 128, 0, 1);
}

#fancyPlacedElement {
  top: 100px;
}
```

```
```


