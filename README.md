# capitalize

Capitalize the first letter of a string, or all words in a string.

## Install

    npm install js-capitalize

## Synopsis

Capitalize the first letter of a string:

```javascript
var capitalize = require('./') // you must import like **require('js-capitalize')**

var test = require('tape')

test('Capitalize first letter', function (t) {
  t.plan(1)
  t.equal(capitalize("united states"), "United states")
})
```

Or capitalize each word in a string:

```javascript
test('Capitalize each word', function (t) {
  t.plan(1)
  t.equal(capitalize.words("united states"), "United States")
})
```

Thanks to [@c990802](https://github.com/grncdr/js-capitalize/pull/2) and [Stack Overflow](http://stackoverflow.com/questions/20690499/concrete-javascript-regex-for-accented-characters-diacritics), capitalize handles international characters:

```javascript
test('Capitalize words with international characters', function (t) {
  t.plan(1)
  t.equal(capitalize.words('hello-cañapolísas'), 'Hello-Cañapolísas')
})
```

and thanks to [@ultraflynn](https://github.com/grncdr/js-capitalize/pull/3), capitalize properly handles quotes within the string:

```javascript
test('Capitalize each word, ignoring quotes', function(t) {
    t.plan(1)
    t.equal(capitalize.words("it's a nice day"), "It's A Nice Day")
})
```

and thanks to [@marceuy](https://github.com/grncdr/js-capitalize/pull/7), Add support for strings with any original case:

```javascript
test('Capitalize upper case words', function(t) {
    t.plan(1)
    t.equal(capitalize("CONGRATULATIONS THIS IS A NICE TEST"), "Congratulations this is a nice test")
})
```

## License

MIT
