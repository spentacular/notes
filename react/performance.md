### Performance
###### Gotta go fast

—

#### Highlight Updates

Highlight components when they update. Colors go from blue > green > yellow > red.

![highlight-updates](https://user-images.githubusercontent.com/1043478/36636442-2c0392b2-198d-11e8-95b9-1ba7ac8e9fea.png)

—

#### Redux Container Components

Directly from the [Redux docs](https://redux.js.org/basics/usage-with-react):

> You could write a container component by hand, but we suggest instead generating container components with the React Redux library's connect() function, which provides many useful optimizations to prevent unnecessary re-renders. (One result of this is that you shouldn't have to worry about the React performance suggestion of implementing shouldComponentUpdate yourself.)

Limit how much `mapStateToProps` you map to a container since you get this free optimzation. The more state you use the higher chances of a render update, which effects every component nested in it.

—

#### Redux Connect Options

You can get the render count for the connected component by passing the following:

```js
export default(
  mapStateToProps,
  mapDispatchToPops,
  mergeProps,
  // options
  {
    // Connected component is passed an additional prop with name renderCount
    renderCountProp: 'renderCount'
  }
)(ConnectComponent)
```

[Redux `connectAdvanced` options](https://github.com/reactjs/react-redux/blob/master/docs/api.md#connectadvancedselectorfactory-connectoptions)

—

#### Articles

- [Twitter Lite and High Performance React Progressive Web Apps at Scale](https://medium.com/@paularmstrong/twitter-lite-and-high-performance-react-progressive-web-apps-at-scale-d28a00e780a3)
