# Event-Bubbling-and-Event-Capturing

## Event Bubbling or Event Capturing?

There are two ways of event propagation in the HTML DOM, `bubbling` and `capturing`.

`Event propagation` is a way of defining the element order when an event occurs. If you have a <p> element inside a <div> element, and the user clicks on the <p> element, which element's "click" event should be handled first?

In bubbling the inner most element's event is handled first and then the outer: the <p> element's click event is handled first, then the <div> element's click event.

In capturing the outer most element's event is handled first and then the inner: the <div> element's click event will be handled first, then the <p> element's click event.

With the addEventListener() method you can specify the propagation type by using the "useCapture" parameter:

```js
 addEventListener(event, function, useCapture);
```

  
The default value is false, which will use the bubbling propagation, when the value is set to true, the event uses the capturing propagation.

Example
 
```js
document.getElementById("myP").addEventListener("click", myFunction, true);
document.getElementById("myDiv").addEventListener("click", myFunction, false);
```
