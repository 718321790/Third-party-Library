# Third-party-Library
常用的一些第三方库

### 1.大数计算
[bignumber.js](https://github.com/MikeMcl/bignumber.js)
```
function addNum(value) {
  const num1 = BigNumber(this)
  const num2 = BigNumber(value)
  const sum = num1.plus(num2)
  return sum.toNumber()
}
String.prototype.add = addNum
Number.prototype.add = addNum
```
