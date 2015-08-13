# Callback

```javascript
function callback1(parametr1) {
    console.log(parametr1)
}

var callback2 = function(parametr1) {
    console.log(parametr1)
}

element.addEventListener('click', callback1)
element.addEventListener('click', callback2)

// callback1({ /* event object */ })
```

# setTimeout

```javascript
function callback() {
    console.log('ahoj')
}

setTimeout(callback, 2000) // 2 s
```

# typeof

```javascript
console.log(typeof "ahoj")
console.log(typeof "ahoj" === "string")
console.log(typeof 42)
console.log(typeof NaN)
```

# !!bool

```javascript
var promenna = "truthy nebo falsy?"
console.log(promenna)
console.log(!promenna) // bool negace
console.log(!!promenna) // bool negace negace
```

# truthy ? "ano" : "ne"

```javascript
var promenna = true

var druha_promenna = promenna ? "ano" : "ne"

console.log(druha_promenna) // "ano"
```

# truthy && "ano"

```javascript
var promenna = true && "ano"
console.log(promenna) // "ano"
```

# falsy || "ano"

```javascript
var promenna1 = true || "ne"
var promenna2 = false || "ne"
console.log(promenna1) // true
console.log(promenna2) // "ne"
```

# Anonymní funkce

```javascript
function() { console.log("toto se neprovede") }

function zavolejArgument(funkce) {
    funkce("tohle jí předám jako param")
}

zavolejArgument(function(param){
    console.log("param: " + param)
})

zavolejArgument(function(param){
    console.log("param: " + param)
})

zavolejArgument(function(param){ console.log("param: " + param)})

zavolejArgument((param) => console.log("param: " + param))

zavolejArgument(param => console.log("param: " + param))

```

# Anonymní objekty

```javascript
function vypisJmeno(obj) {
    console.log(obj.name)
}

var matej = {
    name: "Matěj",
    surname: "Šimek"
}

vypisJmeno(matej)

vypisJmeno({ name: "Vilík", surname: "Kopecký" })
```

# Anonymní self invoking funkce

```javascript
(function(){
    var promenna = 2
})()

console.log(typeof promenna) // "undefined"

(function(x){
    console.log(x) }
)(42)

```

# call, bind, apply

```javascript
function zkouska(param1, param2) {
    console.log(this, param1, param2)
}

zkouska("a", 42) // [Window], "a", 42

var objekt = {}

zkouska.call(objekt, "b") // [objekt], "a", undefined

zkouska.apply(objekt, [ "c", 123 ]) // [objekt], "c", 123

zkouska.bind(objekt) // Function
```

# [].join.call(things, ',')

```javascript
var obj = { 0: "a", 1: "b", length: 2 };
[].join.call(obj, ',')
```

# Chaining

```javascript
var obj = {}

obj.chainA = function() {
    console.log('A')
    return obj
}

obj.chainB = function() {
    console.log('B')
    return obj
}

obj.chainA().chainB().chainB().chainA() // "A", "B", "B", "A"

obj
    .chainA() // "A"
    .chainB() // "B"
    .chainB() // "B"
    .chainA() // "A"
```


# Promises

```javascript

var promise = fetch("/soubor.json")

promise.then(function(data){
    // všechno dobré
    console.log(data)
})

promise.fail(function(data){
    // nastala chyby
    console.error(data)
})

```
