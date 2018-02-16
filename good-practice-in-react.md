# Good Practice in React

Mostly, good pratice dicussed here is about good performance. Here are some rules to follow to [avoid reconciliation](https://reactjs.org/docs/optimizing-performance.html#avoid-reconciliation).

## Use `shouldComponentUpdate()` when needed

When the props or states are changed in :

1. component's `render()` is called to return vitural DOM
1. if the newly returned virtual DOM is different from previously returned one, then DOM nodes are re-rendered; otherwise, DOM nodes are not re-rendered

This is smart but not enough. Sometimes the invocation of `render()` is not necessary. When it is unnecessary, we'd better have a way to not do it--the way to make React not even call `render()` is to let `shouldComponentUpdate()` return `false`.

## Use `React.PureComponent` instead of `React.Component` when it fits

> In most cases, instead of writing `shouldComponentUpdate()` by hand, you can inherit from `React.PureComponent`. It is equivalent to implementing `shouldComponentUpdate()` with a **shallow** comparison of current and previous props and state.

So, "when it fits" is "when only a shallow comparison is enough."

## Do not mutate

`React.PureComponent` only does `shouldComponentUpdate()` with a **shallow** comparison. This means if the porps objects or the state object are mutated, the component will not be re-rendered.

There are some ways to do so and one of the quick ways is to use object spread syntax (over `Object.assign()`) to return a new object.
