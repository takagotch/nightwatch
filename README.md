### nightwatch
---
https://github.com/nightwatchjs/nightwatch

```
npm install nightwatch
git clone https://github.com/nightwatchjs/nightwatch.git
cd nightwatch
npm install

npm test
npm run mocha-coverage

nightwatch examples/tests/googleDemoTest.js
```

```js
module.exports = {
  '' : function(client){
    client
      .url('http://www.google.com')
      .waitForElementVisible('body', 1000)
      .assert.title('Google')
      .assert.visible('input[type=text]')
      .waitForElementVisible('button[name=btnG]', 1000)
      .click('button[name=btnG]')
      .pause(1000)
      .assert.containsText('ol#rso li:first-child',
        'Rembrandt - Wikipedia')
      .end();
  }
};
```

```
```


