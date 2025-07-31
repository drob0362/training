# Context

Context should be used for data which is used all across the application, e.g. a user object.

A context, when created should indicate the shape of what it will hold.

# Using context

Need to wrap components with a `<Context.Provider>` tag, to get app to work with context. Visibility thing.
In React 19, can just use `<Context>` and drop `Provider`.
Context can be used in place of state, once defined.

Don't need to define the setter from useContext if not using it. Can just define the cart variable as follows: `const [cart] = useContext(CartContext)`

The context can then be used in place of state, whereever some common data is used.
