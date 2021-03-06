---
title: umd
tags:
- javascript
- modüller
---

**Universal Module Definition** ifadesinin kısaltması. Bir kodun hem tarayıcıda hem de Node.js üzerinde çalışmasını sağlayan modül tanımlama sistemi.

Birçok yöntem olmakla birlikte, en genel yöntemlerden biri aşağıdaki gibidir:

```js
(function(root, factory) {
  if (typeof define === 'function' && define.amd) {
    // AMD
    define(['b'], factory);
  else if (typeof module === 'object' && module.exports) {
    // Node, CommonJS
    module.exports = factory(require('b'));
  } else {
    // Tarayıcı
    root.web = factory(root.b);
  }
})(typeof self !== 'undefined' ? self : this, function(b) {
  // Modülün kendisi
  return {};
});
```
