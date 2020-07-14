# Ship City

This is a programming challenge. I tried and failed to solve this mathematically.

Hundreds of ships would like to dock to eachother to build a floating city of ships.

Although they are all bound to each other, any ship must be able to leave the collective without needing to ask any other ship to move.

This means they always need to have a route to get to open waters.

However to maintain physical stability against the waters, there should be a route to be able to walk from one ship to any other ship.

### Examples

Here is an example 2x2 grid of ships bounded together, but free to leave to open waters:

    ^^
    v>
    
* The top two ships are pointing up.
* The bottom left ship is pointing down.
* The bottom right ship is pointing right.

They all have access to leave the open water, and are bound as close as possible.

Here is an example 3x3 grid of ships bounded together, but free to leave to open waters:

    ^^^
    < >
    vvv

Notice how all ships have the ability to leave, yet there is a route to get from one ship to any other ship.

This example however is not valid:

    ^^^
    > <
    vvv

Here, the middle ships don't have access to open water. They would run into eachother.

This example is also not valid:

    ^^^
       
    vvv

This is not valid because there must be a route to be able to walk from one ship to any other ship.

Now lets go to 4x4:

    ^^^^
    <  >
    <  >
    vvvv

Although this is a nice and simple design. It is not the most compact. The ships would like to be as compact as possible while still adhering to the rules above.

Here is a more compact design:

    ^^^^
    <v>
      <>
    vvvv
    
    
Notice, all of the ships have access to leave to open waters, yet there is still a route from one ship to get to any other ship.

This is the most compact tiling that I was able to come up with. Out of 16 spaces, 13 are taken.

### The Challenge

Given a n x n size of the city, what is the most compact tiling possible for all of the ships?
