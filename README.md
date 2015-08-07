# ákolen’ JS+DOM

## ~~JavaScript~~ ECMAScript 6

### Z‡kladn’ syntax
- podob‡ se Jav, C (...)
- Unicode
- case sensitive
- instrukce programu se nazùvaj’ vùrazy (expression)

Vùraz:
```js
expression;
```

Koment‡Şe:
```js
// comment
/* 
	multiline
	comment
*/
```

Blok:
```js
if(condition) {
	// obsah bloku
}
```

Funkce:
```js
function example(argument, argument2)Ê{
	// blok funkce
}
```

### Promnn

#### Deklarace:
- kl’‹ov‡ slova: var, let, const

```js
var variable = value;
```

#### Obor pósobnosti - Variable scope:
```js
globalScope = smth;
var functionScope = smth;
let blockScope = smth;
const blockScope = 123;
```

### Datov typy
- dynamickù jazyk = promnn nemaj’ pevn stanovenù datovù typ

#### Primitivn’:

- boolean `true`, `false`
- null
- undefined
- number `123`, `10.05`
- string `'Şetzec'`, `"druhù Şetzec"`
- symbol `var id = Symbol()`

Promnn‡ je pŞ’mo dan‡ hodnota...  

#### Referen‹n’:

- Object `obj = { property: value, prop2: val2 }`
- function `function name(arguments) { body }`

Hodnota promnn je odkaz do pamti na danù objekt...

#### Programov konstrukce

##### pole
```js
var array = [1, 2, 3, 4, 5];
var arrayOfArrays = [
	[ 1, 2, 3, 4, 5 ],
	[ 'cos', 'to', 'Honzo', 'cos', 'to', 'snd' ],
	[ ]
];
// PŞ’stup k hodnot 
array[index];
arrayOfArrays[index][index2];
```

##### objekty
```js
var object = { jedna: 1, dve: 2, tri: 3 };
// PŞ’stup k hodnot
object.jedna;
object['dve'];
```

##### podm’nky
```js
if (condition) { 
	// ...
}

if (...) { ... }
else { ... }

if (...)Ê{ ... }
else if (...) { ... }
```
Hodnoty vyhodnocen jako `false`: `undefined, null, 0, NaN, ""`

Porovn‡vac’ oper‡tory:
- ekvivalence `==`
- neekvivalence `!=`
- striktn’ rovnost `===`
- striktn’ nerovnost `!==`
- vtä’ neì, menä’ neì `>`, `<`
- vtä’ anebo rovno, menä’ anebo rovno `>=`, `<=`

Logick oper‡tory:
- NOT (negace) `!`
- OR (nebo) `one || two`
- AND (a z‡roveË) `one && two`

##### iterace a smy‹ky

```js
// Iterace
for ([initialExpression]; [condition]; [incrementExpression])
  statement

for (variable in object) {
  statements
}

// Cyklus 
do
  statement
while (condition);

while (condition)
  statement
```

##### funkce

```js
function add(first, second) {
	return first + second;
}

var result = add(1, 1);

// Arrow functions
var sum = (first, second) => first + second;

var result2 = sum(1, 2);
```