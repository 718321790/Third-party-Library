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

### 2.获取excel内容
[xlsx](https://github.com/SheetJS/sheetjs)
```
var file = document.querySelector('#fileInput')
file.addEventListener('change', function () {
  var reader = new FileReader()
  reader.onload = function (e) {
    var bstr = e.target.result;
    var wb = XLSX.read(bstr, {type:'binary'});
    /* Get first worksheet */
    var wsname = wb.SheetNames[0];
    var ws = wb.Sheets[wsname];
    /* Convert array of arrays */
    var data = XLSX.utils.sheet_to_json(ws);
  }
  reader.readAsBinaryString(this.files[0]);
})
```
### 3.一些常用的网址
1. [https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/MapLinks/MapLinks.html](苹果地图文档)
