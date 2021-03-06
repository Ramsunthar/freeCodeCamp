---
id: 5cdafbd72913098997531681
title: 在 then 中处理 Promise 完成的情况
challengeType: 1
forumTopicId: 301203
---

# --description--

当程序需要花费未知的时间才能完成时 Promise 很有用（比如，一些异步操作），一般是网络请求。网络请求会花费一些时间，当结束时需要根据服务器的响应执行一些操作。这可以用 `then` 方法来实现，当 promise 完成 `resolve` 时会触发 `then` 方法。例子如下：

```js
myPromise.then(result => {
  // do something with the result.
});
```

`result` 即传入 `resolve` 方法的参数。

# --instructions--

给 promise 添加 `then` 方法。用 `result` 做为回调函数的参数并将 `result` 打印在控制台。

# --hints--

应该给 promise 方法调用 `then` 方法。

```js
assert(codeWithoutSpaces.match(/(makeServerRequest|\))\.then\(/g));
```

`then` 方法应该有一个回调函数，回调函数参数为 `result`。

```js
assert(resultIsParameter);
```

应该打印 `result` 到控制台。

```js
assert(
  resultIsParameter &&
    codeWithoutSpaces.match(/\.then\(.*?result.*?console.log\(result\).*?\)/)
);
```

# --solutions--

