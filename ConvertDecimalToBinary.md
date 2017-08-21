### Solution in JavaScript:
****

``` javascript

  var convertDecimalToBinary = function (decimal) {
    var binaryBase = 2;
    var binary = [];
    var remainder;
    while (decimal !== 0) {
        remainder = decimal % binaryBase;
        decimal = Math.floor(decimal/binaryBase);
        binary.unshift(remainder);
    }
    return binary.join("")
};

```

***
*_Explanation:_*
