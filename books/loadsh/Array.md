
**chunk**
- array:Array
- size:Number
```javascript
  function chunk(array, size) {
    var length = array == null ? 0 : array.length;
    if (!length || size < 1) {
      return [];
    }
    var index = 0,
      resIndex = 0,
      result = Array(Math.ceil(length / size));

    while (index < length) {
      result[resIndex++] = array.slice(index, (index += size));
    }
    return result;
  }
```

**compact**
- array:Array
```javascript
function compact(array) {
  var index = -1,
      length = array == null ? 0 : array.length,
      resIndex = 0,
      result = [];

  while (++index < length) {
    var value = array[index];
    if (value) {
      result[resIndex++] = value;
    }
  }
  return result;
}

```
**difference**
- array:Array
- values:Array
```javascript
function difference(array, values) {
            var index = -1,
                length = array.length,
                result = [],
                valuesLength = values.length;
            outer:
            while (++index < length) {
                var value = array[index];
                var valuesIndex = valuesLength;
                while (valuesIndex--) {
                    if (values[valuesIndex] === value) {
                        continue outer;
                    }
                }
                result.push(value);
            }
            return result;
        }
```

**diffrenceBy**
- array
- values
- iteratee

```javascript
 function differenceBy(array, values, iteratee) {
            var index = -1,
                length = array.length,
                result = [],
                valuesLength = values.length;
            values = values.map(item => {
                if (typeof iteratee == 'function') {
                    return iteratee(item)
                } else if (typeof item == 'object') {
                    return item[iteratee]
                }
            })
            outer:
            while (++index < length) {
                var value = array[index];
                var computed;
                if (typeof iteratee == 'function') {
                    computed = iteratee(value)
                } else if (typeof item == 'object') {
                    computed = value[iteratee]
                }
                var valuesIndex = valuesLength;
                while (valuesIndex--) {
                    if (values[valuesIndex] === computed) {
                        continue outer;
                    }
                }
                result.push(value);
            }
            return result;
        }
```