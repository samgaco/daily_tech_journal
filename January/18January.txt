### 18 of January

Reading about JSX and the virtual DOM in react.


| Tools/Concepts        | Are           | Reference  |
| ------------- |:-------------:| -----:|
|   JSX  | if-else in JSX | [if-else JSX](https://react-cn.github.io/react/tips/if-else-in-JSX.html) |
|   JSX | in depth | [In depth guide](https://reactjs.org/docs/jsx-in-depth.html)

### JSX Attribute expressions

```
const component = (< Alert
                      color={warningLvel === 'debug'? 'gray' : 'red'}
                        log={true} /> )

```

### JSX Spread syntax

```
const props = {msg: "hi", isOpen: true}
<Component {...props} />
it's the same as <Component msg={"hi"} isOpen={true} />
```


### class name npm package

Allows to create an object with classes that will be displayed conditionally.

```
const klass = ({
box: true, // always applied
alert: this.props.isAlert, //only if the prop is set
time: false // never applied
});

return(<div className={klass} />)
```