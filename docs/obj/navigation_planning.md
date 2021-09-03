# Navigation Planning
 
Navigation planning involves the declaration and execution of various components in order for a mobile thingy (a `robot` object) to travel in a designated way in the physical real world.

There are various objects available for navigation planning in **_Diego_**, which can conveniently be depicted in the 'route matrix'...

| ![Route Matrix](../../_img/route_matrix.jpeg "Route Matrix") |
| :---: |
| *Route Matrix* |

Each column of the 'route matrix' are a _'family'_ of objects used for navigation planning. The left column (blue objects) represent the location only navigation planning objects. These objects require at least coordinates to be effective. From the bottom of the column up, the `waypoint` The object is representation of an intermediate physical point or place on a route or line of travel, or simply, a stopping point. Next is the `path` object, which in the strictest terms is a collection of two waypoints and their relationship to each other but only in terms of location.  The `route` object is a collection of `path`s arranged in a logical order with relationships defined for each `path`.  For each `route` object there are man `path`s. The `itinerary` is the top-most location-only navigation planning object.

In a similar fashion to the location-only objects, the green objects have similar scope to their adjacent objects.  The green object represent the orientation objects, that have location **and** orientation attributes.  The `excurs`_(ion)_ object has many `course` objects, each `course` object has many `way` objects, an each `way` object has usually two `pose` (or `posepoint`) objects.

The orange objects are known as the logging navigation planning objects, as they log the 'journey' between `goal`s. The `tour` object has many `journey` objects, each `journey` object has many `trip` objects, an each `trip` object has usually two `goal`s.  The attributes if the logging navigation planning objects are location **and** orientation **and** time-logging.
