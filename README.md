# \<caja-sanitizer\>



## Import the sanitizer
```<link rel="import" href="../bower_components/caja-sanitizer/caja-sanitizer.html">```

## Insert the Element

```
<caja-sanitizer id="cajaSanitizer"></caja-sanitizer>
```


## Call the sanitizer
The response will be a promise
```
const dirtyString = "<p>Hello, <b onclick=alert(1337)>World</b>!</p>"
this.$.cajaSanitizer.sanitize(dirtyString)
.then((sanitized) => {
    console.debug(sanitized)
})
.catch((err) => {
    console.error(err)
})
```

## Pass to the sanitizer

```
<caja-sanitizer input="[[input]] output="{{output}}"></caja-sanitizer>
```


