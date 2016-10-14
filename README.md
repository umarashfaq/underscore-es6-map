# underscore-es6-map

## Collection Functions

###  \_.each

```javascript
// ARRAY
// -----

// underscore
_.each([1, 2, 3], alert);

// ES6
[1, 2, 3].forEach(alert);

// OBJECT
// ------

// underscore
_.each({one: 1, two: 2, three: 3}, alert);

// ES6
const obj = {one: 1, two: 2, three: 3}
Object.keys(obj).forEach(key => alert(obj[key]))
```

###  \_.map

```javascript
// ARRAY
// -----

// underscore
_.map([1, 2, 3], function(num){ return num * 3; });

// ES6
[1, 2, 3].map(num => num * 3);

// OBJECT
// ------

// underscore
_.map({one: 1, two: 2, three: 3}, function(num, key){ return num * 3; });

// ES6
const obj = {one: 1, two: 2, three: 3};
Object.keys(obj).map(key => obj[key] * 3);
```

###  \_.reduce

```javascript
// ARRAY
// -----

// underscore
var sum = _.reduce([1, 2, 3], function(memo, num){ return memo + num; }, 0);

// ES6
const sum = [1, 2, 3].reduce((memo, num) => memo + num, 0);
```

###  \_.reduceRight

```javascript
// ARRAY
// -----

// underscore
var list = [[0, 1], [2, 3], [4, 5]];
var flat = _.reduceRight(list, function(a, b) { return a.concat(b); }, []);

// ES6
const list = [[0, 1], [2, 3], [4, 5]];
const flat = list.reduceRight((a, b) => a.concat(b), []);
```

###  \_.find

```javascript
// ARRAY
// -----

// underscore
var even = _.find([1, 2, 3, 4, 5, 6], function(num){ return num % 2 == 0; });

// ES6
const even = [1, 2, 3, 4, 5, 6].find(num => num % 2 == 0);
```


###  \_.filter

```javascript
// ARRAY
// -----

// underscore
var evens = _.filter([1, 2, 3, 4, 5, 6], function(num){ return num % 2 == 0; });

// ES6
const evens = [1, 2, 3, 4, 5, 6].filter(num => num % 2 == 0);
```

###  \_.where

```javascript
// ARRAY
// -----

// underscore
_.where(listOfPlays, {author: "Shakespeare", year: 1611});

// ES6
listOfPlays.filter(({author, year}) => author === "Shakespeare" && year === 1611);
```

###  \_.findWhere

```javascript
// ARRAY
// -----

// underscore
_.findWhere(publicServicePulitzers, {newsroom: "The New York Times"});

// ES6
publicServicePulitzers.filter(({newsroom}) => newsroom === "The New York Times");
```


###  \_.reject

```javascript
// ARRAY
// -----

// underscore
var odds = _.reject([1, 2, 3, 4, 5, 6], function(num){ return num % 2 == 0; });

// ES6
const odds = [1, 2, 3, 4, 5, 6].reject(num => num % 2 !== 0);
```
