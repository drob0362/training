# How it works

Tanstack router works by the link between a specific file which imports the Tanstack router. A specific component from the Tanstack library, called `Outlet` must be used in the page importing the router.

There is a bit of magic going on, as the TR creates a file for us (`routeTree.gen`) which presumably contains information about the routes which exist.

Routes have to be explicity created in files which relate to specific url paths or routes.

To utilise the routes, create and use a TR router object as a parameter of the Tanstack `RouterProvider` component.
