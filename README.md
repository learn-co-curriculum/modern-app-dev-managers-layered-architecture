# Layered Architecture

## Learning Goals

- Explain how layers can simplify the organization of large systems.
- Explain vertical and horizontal layers.

## What are Layers?

We interact with complex systems every day such as cars, computers,
transportation networks. These systems provide easy ways for users to interact
with them without necessarily understanding exactly how they work. For example,
we can drive cars without knowing how an engine works, use computers without
knowing how processors work, and can send packages across the country without
knowing transportation logistics.

Large systems can be broken down into layers to make their complexity more
manageable. A single layer handles a specific part of the system and enables
interaction between the layers. Let’s look at a concrete example to better
understand the concept of layers.

## How is a Package Delivered Across the Country?

Let’s imagine we want to send an item from NYC to California. It takes several
sub systems to work in harmony to ensure that the item is properly delivered.

![Untitled](https://curriculum-content.s3.amazonaws.com/modern-app-dev-managers-leadership/layered-architecture/01.png)

Here are the general steps:

1. A sender packages the item.
2. The sender selects a delivery service and has the package picked up by a
   carrier.
3. The carrier office decides how to send the package and schedules the
   delivery.
4. The package is transported using various vehicles to the receiver’s city.
5. Different transportation services may be used depending on the locality.
6. The receiver’s local carrier office schedules delivery to the receiver’s
   house.
7. A carrier picks up the package from the carrier office.
8. The package is delivered to the receiver.

The sender doesn’t have to know how any of the layers work here to be able to
send the package. All the complexities is handled by the other layers.

### Vertical Layers

Notice that each layer is passing the package to the next layer. For example,
the carrier provides service to the sender and the receiver. They collect, sort,
and deliver packages to the houses. All the sender has to know is how to package
an item and select a carrier service.

How does this translate to network layers? The top layer is usually called an
****************\*\*****************application
layer****************\*\*****************. A user can interact with the
application without knowing anything about the layers. For instance, we can use
an email application without understanding how an email service works. This
layer abstracts the functionality and hides all the implementation details from
the user.

### Horizontal Layers

In the package example, similar layers deal with similar levels of complexity
and are more aware of their layer’s internal workings over the other layers’
details. For example, the carrier offices can directly communicate with each
other but they can’t dictate exactly how a transportation vehicle navigates to
its destination.

In networks, the layers are even more isolated from each other. For example,
applications layers can send and receive data between each other. An application
layer has a parallel on another end-user system such as when a chat app can send
a message to a chat app on another system. To the user of this layer, it may
seem as though the layers are communicating directly with each other.

## Benefits of Separating Systems into Layers

There are several benefits to breaking down systems like this:

1. Provides abstractions that users can work with more easily.
2. Layers can be developed independently of each other, i.e., the mechanism of a
   layer can be changed without affecting its communication with other layers so
   long as it follows a specified protocol.
3. Layers can be managed by different groups. In the package example, different
   companies can provide the carrier and transportation service so long as they
   agree on how to exchange packages between them.

## Conclusion

This idea of breaking down systems into smaller, self-contained, modular parts
comes up over and over again when developing complex systems. It’s not possible
for a single entity to design, iterate, and develop everything. Breaking things
down not only makes development easier, but also allows a better experience for
the end-user.
