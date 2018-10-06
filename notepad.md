## React For Beginners

Avoid binding process functions by instead declaring them as properties directly bound to the instance.

```javascript
//Instead of this:
constructor() {
  super();
  this.doTheThing = this.doTheThing.bind(this)
}
function doTheThing(params) {..

//Consider this:
doTheThing = (params) => {...
```

In order to gather the data from from forms or input fields, react uses special properties known as _references_ or _refs_.

To use a ref, simply delare it using the `createRef()`

```javascript
myInput = React.createRef();

displayInput = () => console.log(this.myInput.value.value);
//returns "this is an example"

render() {
  return (
    <input
      type="text"
      ref="{this.myInput}" defaultValue="this is an example"
    />
  )
}
```
