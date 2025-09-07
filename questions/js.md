<h3> <img src="../assets/JavaScript.png" width="16" height="16" /> <span>JavaScript:</span> </h3>

<details> <summary>Типы данных в JavaScript?</summary>

Ответ:
В JS есть 8 типов данных:

Примитивы: string, number, bigint, boolean, null, undefined, symbol.

Объект (object).

typeof "hello" // "string"
typeof 42 // "number"
typeof null // "object"
typeof {} // "object"

</details>
<details> <summary>Разница между `==` и `===`?</summary>

Ответ:

== — сравнивает с приведением типов.

=== — строгое сравнение.

5 == "5" // true
5 === "5" // false

</details>
<details> <summary>Что такое Strict mode?</summary>

Ответ:
"use strict" — строгий режим, запрещает опасные действия и включает больше ошибок.

"use strict";
x = 3.14; // ReferenceError

</details>
<details> <summary>Function declaration vs function expression?</summary>

Ответ:

Declaration — можно вызвать до объявления.

Expression — только после.

sayHi(); // ✅
function sayHi() {}

sayBye(); // ❌
const sayBye = function() {};

</details>
<details> <summary>Разница между `null` и `undefined`?</summary>

Ответ:

null — "нет значения", задаётся явно.

undefined — переменная объявлена, но не имеет значения.

let a; // undefined
let b = null;

</details>
<details> <summary>Типы таймеров?</summary>

Ответ:

setTimeout

setInterval

clearTimeout, clearInterval

setTimeout(() => console.log("1 раз"), 1000);
setInterval(() => console.log("каждую секунду"), 1000);

</details>
<details> <summary>Что такое Hoisting?</summary>

Ответ:
Поднятие объявления переменных и функций вверх области видимости.

console.log(a); // undefined
var a = 5;

</details>
<details> <summary>Что такое Scope?</summary>

Ответ:
Область видимости — часть кода, где доступна переменная:

глобальная

функциональная

блочная (для let/const)

</details>
<details> <summary>Разница между var, let и const?</summary>

Ответ:

var — функциональная область, hoisting.

let — блочная область.

const — блочная область, нельзя переопределять.

var a = 1; let b = 2; const c = 3;

</details>
<details> <summary>Что такое замыкание?</summary>

Ответ:
Функция, которая запоминает переменные из внешней области.

function outer() {
let count = 0;
return () => ++count;
}
const inc = outer();
inc(); // 1
inc(); // 2

</details>
<details> <summary>Что обозначает this?</summary>

Ответ:
Значение this зависит от контекста вызова:

в объекте — сам объект

в функции — undefined (в strict) или window

в классе/методе — экземпляр

</details>
<details> <summary>Функции высшего порядка?</summary>

Ответ:
Функции, которые принимают другие функции или возвращают их.

function hof(fn) { return fn(5); }
hof(x => x\*2); // 10

</details>
<details> <summary>Как превратить в boolean? Ложные значения?</summary>

Ответ:
Через Boolean(value) или !!value.
Falsy: 0, "", null, undefined, NaN, false.

!!"hello" // true
!!0 // false

</details>
<details> <summary>Методы строк?</summary>

Ответ:
toUpperCase(), toLowerCase(), includes(), slice(), split(), trim(), replace() и др.

"hello".toUpperCase(); // "HELLO"

</details>
<details> <summary>Методы массивов?</summary>

Ответ:

изменяют: push, pop, shift, unshift, splice

не изменяют: map, filter, forEach, reduce, slice, find, some, every

</details>
<details> <summary>Что такое чистая функция?</summary>

Ответ:
Функция, которая:

не изменяет внешние данные,

всегда возвращает один результат для одинаковых входных.

function add(a,b){ return a+b }

</details>
<details> <summary>Разница между .forEach() и .map()?</summary>

Ответ:

forEach — перебор, ничего не возвращает.

map — создаёт новый массив с результатами.

[1,2,3].forEach(x => console.log(x*2));
[1,2,3].map(x => x*2); // [2,4,6]

</details>
<details> <summary>Разница между call, apply и bind?</summary>

Ответ:

call(this, ...args) — вызывает с контекстом и аргументами.

apply(this, [args]) — то же, но принимает массив.

bind(this) — возвращает новую функцию.

function hi(a,b){ console.log(this.name,a,b) }
hi.call({name:"Bob"},1,2);
hi.apply({name:"Bob"},[1,2]);
const f = hi.bind({name:"Bob"});
f(1,2);

</details>
<details> <summary>Почему функции — объекты первого класса?</summary>

Ответ:
Функции можно:

присваивать переменным

передавать как аргументы

возвращать из других функций

</details>
<details> <summary>Как определить наличие свойства?</summary>

Ответ:

"prop" in obj

obj.hasOwnProperty("prop")

let user = {name:"Tom"};
"name" in user; // true

</details>
<details> <summary>Что такое IIFE?</summary>

Ответ:
Immediately Invoked Function Expression — функция, которая выполняется сразу после объявления.

(function(){ console.log("run") })();

</details>
<details> <summary>Что такое arguments?</summary>

Ответ:
Псевдомассив всех аргументов функции (в ES6 лучше ...rest).

function sum(){ return [...arguments].reduce((a,b)=>a+b) }

</details>
<details> <summary>Разница host и native объектов?</summary>

Ответ:

Host — предоставлены окружением (DOM, XMLHttpRequest).

Native — встроены в язык (Array, Object, Function).

</details>
<details> <summary>Почему сравнение 2 объектов = false?</summary>

Ответ:
Потому что сравниваются ссылки, а не содержимое.

{} === {} // false

</details>
<details> <summary>Прототипное наследование? Object без прототипа?</summary>

Ответ:
Объекты наследуют свойства от [[Prototype]].
Создать без прототипа:

let obj = Object.create(null);

</details>
<details> <summary>Почему плохо расширять нативные объекты?</summary>

Ответ:
Может привести к конфликтам, сломанной совместимости и непредсказуемым багам.

</details>
<details> <summary>Что такое NaN? Как проверить?</summary>

Ответ:
NaN — Not a Number, результат некорректных операций.
Проверка: Number.isNaN(value).

</details>
<details> <summary>Что такое Wrapper Objects?</summary>

Ответ:
Объектные обёртки для примитивов (String, Number, Boolean).

let str = new String("hi");

</details>
<details> <summary>Как создать объект?</summary>

Ответ:

литерал {}

new Object()

Object.create(proto)

классы/функции-конструкторы

</details>
<details> <summary>Для чего new?</summary>

Ответ:
Создаёт новый объект и связывает его с прототипом конструктора.

function User(name){ this.name=name }
const u = new User("Tom");

</details>
<details> <summary>Операторы && и ||?</summary>

Ответ:

&& — возвращает первое ложное или последнее.

|| — возвращает первое истинное.

false && "a" // false
false || "a" // "a"

</details>
<details> <summary>Для чего !!?</summary>

Ответ:
Приведение к boolean.

!!"hello" // true
!!0 // false

</details>
<details> <summary>Оператор %?</summary>

Ответ:
Остаток от деления.

7 % 3 // 1

</details>
<details> <summary>Как проверить массив?</summary>

Ответ:
Array.isArray(value)

</details>
<details> <summary>Boxing/unboxing?</summary>

Ответ:
JS автоматически оборачивает примитивы в объекты ("hi".toUpperCase()), а потом "разворачивает" обратно.

</details>
<details> <summary>Что такое мемоизация?</summary>

Ответ:
Кэширование результатов функции.

function memo(fn){
const cache={}
return x => cache[x] ?? (cache[x]=fn(x))
}

</details>
<details> <summary>Разница in и hasOwnProperty?</summary>

Ответ:

in — ищет в цепочке прототипов.

hasOwnProperty — только в самом объекте.

</details>
<details> <summary>Deep vs shallow copy?</summary>

Ответ:

Shallow — Object.assign({}, obj), спред {...obj}

Deep — structuredClone(obj), JSON.parse(JSON.stringify(obj))

</details>
<details> <summary>Chaining?</summary>

Ответ:
Вызов методов подряд, возвращая this.

class Calc {
constructor(v=0){ this.v=v }
add(n){ this.v+=n; return this }
mul(n){ this.v\*=n; return this }
}
new Calc(2).add(3).mul(4).v // 20

</details>
<details> <summary>Что такое необъявленная переменная?</summary>

Ответ:
Переменная, не объявленная через let/var/const, но присвоенная → глобальная (в strict — ошибка).

</details>
<details> <summary>Передача параметров?</summary>

Ответ:
Передача по значению, но для объектов — передаётся ссылка (сама ссылка по значению).

</details>
<details> <summary>Что такое прототип объекта?</summary>

Ответ:
Ссылка [[Prototype]], откуда объект наследует свойства/методы.

</details>
<details> <summary>Как работает Object.create()?</summary>

Ответ:
Создаёт новый объект с указанным прототипом.

let proto={sayHi(){console.log("hi")}}
let obj=Object.create(proto);
obj.sayHi();

</details>
<details> <summary>Object.freeze() vs Object.seal()?</summary>

Ответ:

freeze — нельзя менять свойства и добавлять новые.

seal — менять можно, добавлять нельзя.

</details>
<details> <summary>.slice() vs .splice()?</summary>

Ответ:

slice(start,end) — возвращает копию.

splice(start, count, ...items) — изменяет массив.

</details>
<details> <summary>.find(), .findIndex(), .indexOf()?</summary>

Ответ:

find — элемент по условию

findIndex — индекс по условию

indexOf — индекс по значению

</details>
<details> <summary>Плюсы и минусы use strict?</summary>

Ответ:

ловит ошибки

запрещает небезопасные действия
– ломает старый код

</details>
<details> <summary>.push(), .pop(), .shift(), .unshift()?</summary>

Ответ:

push → конец

pop → удалить с конца

shift → удалить с начала

unshift → добавить в начало

</details>
<details> <summary>JSON.parse() vs JSON.stringify()?</summary>

Ответ:

parse — строка → объект

stringify — объект → строка

</details>
<details> <summary>Как создать массив?</summary>

Ответ:
[], new Array(), Array.of(), Array.from().

</details>
<details> <summary>.unshift() и .push()?</summary>

Ответ:

unshift — добавляет в начало.

push — в конец.

</details>
<details> <summary>delete и splice?</summary>

Ответ:

delete arr[i] — удаляет элемент, но оставляет пустое место.

splice(i,1) — удаляет и сдвигает элементы.

</details>
<details> <summary>Разница массивов и объектов?</summary>

Ответ:

массивы — упорядоченные коллекции с индексами

объекты — ассоциативные коллекции "ключ-значение"

</details>
<details> <summary>Оператор typeof?</summary>

Ответ:

typeof null → "object" (ошибка JS)

typeof [] → "object", но Array.isArray([]) → true

</details>
