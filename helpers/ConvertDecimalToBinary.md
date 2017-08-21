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
**_Explanation:_**

``` javascript

convertDecimalToBinary(15);

/*
 * 15 / 2 = 7 remainder 1, 7 is now the value for decimal;
 * 7 / 2  = 3 remainder 1, 3 is now the value for decimal;
 * 3 / 2  = 1 remainder 1, 1 is now the value for decimal;
 * 1 / 2  = 0 remainder 1; We stop here since decimal is now 0;
 * 
 * Join the remainders together to get '1111' so that:
 * 15 base 10 = 1111 base 2
 */

```
