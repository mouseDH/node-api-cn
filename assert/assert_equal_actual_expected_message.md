<!-- YAML
added: v0.1.21
-->

使用相等运算符（`==`）来测试 `actual` 和 `expected` 参数是否相等。

```js
const assert = require('assert');

assert.equal(1, 1);
// 通过，1 == 1
assert.equal(1, '1');
// 通过，1 == '1'

assert.equal(1, 2);
// 抛出 AssertionError: 1 == 2
assert.equal({a: {b: 1}}, {a: {b: 1}});
// 抛出 AssertionError: { a: { b: 1 } } == { a: { b: 1 } }
```

如果两个值不相等，则抛出一个带有 `message` 属性的 `AssertionError`，其中 `message` 属性的值等于传入的 `message` 参数的值。
如果 `message` 参数为 `undefined`，则输出默认的错误信息。

