# Методи кор бо объектҳо дар JavaScript

Ин файл фаҳмиш ва намунаҳои истифодаи муҳимтарин методҳои кор бо объектҳо дар JavaScript-ро пешниҳод мекунад:  
`for...in`, `Object.keys()`, `Object.values()`, `Object.entries()`, ва `Object.fromEntries()`.

---

## 1. for...in — Давра задан бо калидҳои объект

Цикл `for...in` барои давра задан дар ҳама калидҳои (ключҳои) як объект истифода мешавад.

```js
const user = { name: "Ali", age: 25, country: "Tajikistan" };

for (const key in user) {
  console.log(key);          
  console.log(user[key]);    
}
2. Object.keys() — Гирифтани рӯйхати калидҳо
Метод Object.keys() массиви калидҳои объектро бармегардонад.

js
Копировать код
const user = { name: "Ali", age: 25, country: "Tajikistan" };
const keys = Object.keys(user);

console.log(keys); 
3. Object.values() — Гирифтани рӯйхати арзишҳо
Метод Object.values() массиви арзишҳои объектро бармегардонад.

js
Копировать код
const user = { name: "Ali", age: 25, country: "Tajikistan" };
const values = Object.values(user);

4. Object.entries() — Табдил додани объект ба массиви ҷуфтҳо
Метод Object.entries() объектро ба массиви ҷуфтҳои [ключ, значение] табдил медиҳад.

js
Копировать код
const user = { name: "Ali", age: 25, country: "Tajikistan" };
const entries = Object.entries(user);

console.log(entries);
5. Object.fromEntries() — Табдил додани массиви ҷуфтҳо ба объект
Метод Object.fromEntries() баръакс амал мекунад — массиви ҷуфтҳоро гирифта, объект месозад.

js
Копировать код
const entries = [["name", "Ali"], ["age", 25], ["country", "Tajikistan"]];
const user = Object.fromEntries(entries);

console.log(user);
Мисоли пурра
js
Копировать код
const user = { name: "Ali", age: 25, country: "Tajikistan" };

for (const key in user) {
  console.log(`${key}: ${user[key]}`);
}

const keys = Object.keys(user);
console.log(keys);

const values = Object.values(user);
console.log(values);

const entries = Object.entries(user);
console.log(entries);

const newUser = Object.fromEntries(entries);
console.log(newUser);
Хулоса
for...in — давра задан дар объект бар асоси калидҳо

Object.keys() — гирифтани массиви калидҳо

Object.values() — гирифтани массиви арзишҳо

Object.entries() — табдил додани объект ба массиви ҷуфтҳо (ключ ва значение)

Object.fromEntries() — баръакс, аз массиви ҷуфтҳо объект сохттан# lecture-8
