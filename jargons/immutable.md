---
title: immutable
sameWith:
- immutability
tags:
- javascript
- haskell
- ocaml
- fonksiyonel programlama
---

Bu terim, uygulamanın herhangi bir noktasında [mutate](/mutation) edilemeyen veya edilmemesi gereken veri tipleri için kullanılır.

Örnek olarak JavaScript için `const x = 5;` tanımlamasındaki `x` değişkeni immutable'dır. Ya da bir başka örnek olarak `Object` içindeki `freeze` metodu objeyi `immutable` hale getirir,

```js
const obj = { key1: 'value1' };

Object.freeze(a);

a.key2 = 'value2';

console.log(a); // Output: { key1: 'value1' }
```
