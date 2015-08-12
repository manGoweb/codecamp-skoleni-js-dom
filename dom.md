# DOM

- [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) ... co to asi bude?
- sada globálních objektů, které jsou dostupné v prohlížeči
- možnost jak ovlivnit obsah, reagovat na uživatelský vstup, komunikovat se serverem, ukládat data apod.


```js
console.dir(window);
console.dir(document);
```

## Základní typy objektů

### document   

### element 

### nodeList    

### attribute   

### namedNodeMap (element.attributes)

![dom crude map](http://html5tutorial.com/dom-inheritance-map/dom-crude-map.png)


## Nejpoužívanější metody 

- document.getElementById(id)
- element.getElementsByTagName(name)
- document.createElement(name)
- parentNode.appendChild(node)
- element.innerHTML
- element.style.left
- element.setAttribute
- element.getAttribute
- element.addEventListener
- window.onload
- window.scrollTo

## Node

- getComputedStyle

## Selektory

- element.querySelector(selectors)
- element.querySelectorAll(selectors)

## Manipulace 

- [Make an interactive website](https://www.codecademy.com/skills/make-an-interactive-website)

## Events

- Event Propagation - bublání odspoda nahoru
- [DOM Events](http://devdocs.io/dom_events/)

## AJAX

- [XMLHttpRequest](http://devdocs.io/dom/xmlhttprequest/using_xmlhttprequest)
- [fetch](http://devdocs.io/dom/fetch_api/using_fetch)

# HTML5 APIs
- canvas
- audio
- webgl
- drag n drop
- web messaging
- web sockets
- web workers
- web storage
- geo location
- file api
- [...](http://html5index.org)
