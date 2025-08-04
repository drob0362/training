# Intro

[Link](<https://frontendmasters.com/courses/intermediate-next-js/react-standards-in-next-js/>
Course by Scott Moss.

Course makes it clear that a lot of concepts included in Next, are actually part of React, e.g. server
and client side components.

# Topics of interest

These topics are mentioned in the course. Others topics may be present, in the interest
of documenting things I did not know.

- Transitions
- Server/Form Actions
- Streaming

## Server side rendering

All components are server side rendered, unless they are lazy loaded.
Server side components differ from client side components, as they run on the server in addition
to being rendered server side.

## Server Actions

A server action is a function which runs on the server and is called from the client.
Examples included talking to a database, reading the file system. These actions connect forms
to server side functions.

Server actions can only be used within files that contain the `use server` directive.
A server action can be used where previously you would have made an API call.

### Submit button hooks and useFormState

####  useformstate

The `useFormState` hook is the binding between server actions and client components.
The state associated with this hook needs to be used within the form as the `action` parameter.

The hook useFormState returns a tuple containing the form state and the action that can be called.

A hook called `useFormStatus` exists, which when it is used in a component which is a `child` component
of a form which is using a form action, it knows the form status automatically.

The form state `action` is called as a function.

Server actions are always in the scope of a request, the hint being in the word server. Something has occurred on the client, which then results in a
call to the server for some purpose. It is at this point that the action
comes into play. A valid example being form submission.

## Transitions

## Route slots(parallel routes)

Route slots provide a means of conditionally rendering content within
a layout. Route slots can either be created or you can use provided slots.
Slots can also be simultaneously rendered.

Files are organised using the `@folder` convention. Each entry in the file system like this is a slot.
In the parent layout, slots are passed as props.
