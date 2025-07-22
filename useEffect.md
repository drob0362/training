# useEffects

Often use with state, and perhaps forms.
Effects relates to side effects.

Effects are suitable for using when something only needs to occur once, or for specific changes.

The `useEffect` final parameter's purpose is to control when the useEffect will fire.
So for example, if the empty array is used as the parameter - then no parameters are being tracked so it will only occur once. If an actual variable was being used, if the variable changed then the `useEffect` would execute again.
