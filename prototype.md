# Array
## map
```javascript
Array.prototype.mymap = function(callback) {
    const resultArray = [];
    for (let index = 0; index < this.length; index++) {
        resultArray.push(callback(this[index], index, this));
    }
    return resultArray;
}
```
## filter 
```javascript
Array.prototype.mfilter =  function (callback) {
  var filtered = [];
  for(let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) filtered.push(this[i]);
  }
  return filtered;
};


//////////////////////////////////////////////////////////////
Array.prototype.myFilter = function(callback){
  var newArray = [];
  // Add your code below this line
  this.forEach(function(x) {
    if (callback(x) === true) {
      newArray.push(x);
    }
  })
  // Add your code above this line
  return newArray;

};
```

## reduce
```javascript
Array.prototype.reduce2 = function(callback, start){
  var result = start !== undefined ? start : this[0];
  for (var i = 1; i < this.length; i++) {
    result = callback(result, this[i]);
  }
  return result;
}
```
