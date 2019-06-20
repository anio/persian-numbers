
# Persian Numbers


### For Browser and Node.js

```javascript
var latinToPersian = function (text) {
    return text.replace(/[0-9]/g, function($0) {return '۰۱۲۳۴۵۶۷۸۹'[$0|0]})
}

var persianToLatin = function (text) {
    return text.replace(/[\u06F0-\u06F9]/g, ($0) => {return '۰۱۲۳۴۵۶۷۸۹'.indexOf($0)})
}

```

### For Python

```python
import re

def latin_to_persian(text):
    return re.sub('[0-9]', lambda x: u'۰۱۲۳۴۵۶۷۸۹'[int(x.group(0))], text)


def persian_to_latin(text):
    return re.sub(r'[\u06F0-\u06F9]', lambda x: str(u'۰۱۲۳۴۵۶۷۸۹'.index(x.group(0))), text)
```
