# dom-xss-code-review

DOM XSS Sources to grep for:

```javascript
document.URL
document.documentURI
document.URLUnencoded
document.baseURI
location
document.cookie
document.referrer
window.name
history.pushState
history.replaceState
localStorage
sessionStorage
IndexedDB (mozIndexedDB, webkitIndexedDB, msIndexedDB)
Database
```

DOM XSS Sinks to grep for:

```javascript
window.location
eval()
WebSocket()
postMessage()
setRequestHeader()
FileReader.readAsText()
ExecuteSql()
sessionStorage.setItem()
document.evaluate()
JSON.parse()
element.setAttribute()
RegExp()
document.write()
document.writeln()
document.domain
document.cookie
element.src
element.innerHTML
element.outerHTML
element.insertAdjacentHTML
element.onevent
```

jQuery sinks:

```jquery
add()
after()
append()
animate()
insertAfter()
insertBefore()
before()
html()
prepend()
replaceAll()
replaceWith()
wrap()
wrapInner()
wrapAll()
has()
constructor()
init()
index()
jQuery.parseHTML()
$.parseHTML()
```

Javascript sinks:

```javascript
eval()
Function()
setTimeout()
setInterval()
setImmediate()
execCommand()
execScript()
msSetImmediate()
range.createContextualFragment()
crypto.generateCRMFRequest()
```

PostMessage XSS:

```javascript
postmessage()
.addEventListener('message',
```
Reference:
https://portswigger.net/web-security/dom-based/controlling-the-web-message-source

Tools: 
Burp Invader browser
