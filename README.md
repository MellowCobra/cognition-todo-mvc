# Cognition TodoMVC

The intensely boring application -- now without MVC!

## Overview

This application is the TodoMVC application rewritten with the declarative-styled, component-driven **cognition** framework.

Cognition is a client side framework designed for building single page web applications on top of a service based
architecture for data and persistence. Cognition applications are built with encapsulated component definition files called *cogs*.

Cog definitions are lazy-loaded and instanced into a component object tree. Each cog contains it's own the rendering and application logic and is shielded by the framework from naming collisions with other components. For performance
cogs definitions are compiled and cached on first download.

A cog file is an html format file consisting of three root tags: *blueprint*, *display*, and *script*.

The **blueprint** has all the special cognition framework tags.

The **display** is the component template for the cog.

The **script** contains the local variables and methods for the cog in object format.

##Important Cognition tags:

**data** - This tag defines an event generating observable variable on the data bus ([catbus]).

**sensor** - This tag listens for events on the data bus (by default the "change" event) and performs an action.
A sensor can run a local cog method or transform the data and pipe it to another data point.

**cog** - This tag loads a child tag into the cog. The cog will be loaded into a container tag in
the display template based on the element id.

**prop** - This tag finds a data point in a parent cog and makes it accessible to scripts from the "this" context.


## License

Apache V2.0, see LICENSE file.

[catbus]: https://github.com/DarkMarmot/catbus
