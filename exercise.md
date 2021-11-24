#### Browser JS Vs Node JS:
- Each browser uses their own JS engine to run Javascript on client side. But Node JS uses the v8 engine integrated with Chrome which is used on server side.
- Browser restricts the access to the machine (like a sandbox) components. But Node JS comes with modules that make it easy to interact with the machine or 
  environemnt it is running on.
- Browser JS is mostly used to interact with front end components like DOM, cookies, local storage, APIs etc. But node JS is developed to work with Backend thereby
  maintaining consistency across the environemnt. It gives freedom of developing applications just like any general programming language(Java, Go) with out 
  restrictions.
- As each browser implements their own version of ES, they take a long time embrace new features(But babel can be used which is extra work. Based on requirements, 
  one can choose node JS version which is regularly updated to use new features in ES.
- Browsers don't give developers an option of changing the runtime environment their site runs on, so he/she has to use JS which is compatible with all browsers
  that are used by clients. Node JS gives option of choosing their runtime environment(all the libraries, modules that other developers contributed).

#### How browser renders website:
- High level flow of rendering process consists of following steps
  1. Parse HTML: 
     - Forgiving by nature. Even if there are errors, it will try to correct the structure.
     - parse flow: it's a circular process between tokenizer, parse tree, DOM tree, script execution.
     - script, link, style tags can halt the parser. So try to keep script at end of HTML or use defer or async properties.
     - can do speculative parsing where it creates another thread to parse elements that are ahead like script, images, css.
  2. Parse CSS: will create CSS object model which consists of all styles, rules, decorators etc.
  3. Render/Frame tree:
     - Combines both DOM and CSS object model to create a tree which is actual representation of what will be shown on screen.
     - Multiple tress: renderObjects, renderStyles, renderLayers, lineBoxes.
  4. Layout: computes where the nodes actually will be on screen in relation to other elements taking into consideration of css properties.
  5. Paint: computes bitmaps and composites so that an image of the layout can be produced i.e, to give visual output of the page.

#### Sample code session using `typeof`
- output of executing that statement in browser console is given as comment beside that line.
```js
typeof(1);               // "number"
typeof(1.1);             // "number"
typeof('1.1');           // "string"
typeof(true);            // "boolean"
typeof(null);            // "object"
typeof(undefined);       // "undefined"
typeof([]);              // "object"
typeof({});              // "object"
typeof(NaN);             // "number"
```
