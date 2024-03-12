# Fixed Memory Marking for G1 (C++)
This project is done in reference to the course [Project in Software Engineering](https://ssw.jku.at/Teaching/Lectures/PSE/2024SS/index.html) at [JKU](https://www.jku.at/).

The [G1 garbage collector](https://docs.oracle.com/en/java/javase/20/gctuning/garbage-first-g1-garbage-collector1.html#GUID-ED3AB6D3-FD9B-4447-9EDF-983ED2F7A573) is the current default garbage collector in the OpenJDK Hotspot VM. 
Its algorithm to determine reachable objects is a straightforward implementation of the [Tri-Color abstraction](https://en.wikipedia.org/wiki/Tracing_garbage_collection#Tri-color_marking). 
The drawback of this algorithm is that mark stack, a helper data structure, memory requirements is only bounded by the number of live objects which can be a very large number (in the MBs).
There is an [algorithm](https://patents.justia.com/patent/8335806) that bounds only needs a very small mark stack and a small helper table to complete marking.

## Project Description
Implement a marking algorithm that uses (small) constant memory and compare with the existing.

The task for this work comprises:
- [ ] Implement the mentioned algorithm in the G1 garbage collector.
- [ ] The description only describes single-threaded operation, extend it to use multiple threads.
- [ ] Compare its performance and memory consumption to the existing algorithm on benchmarks.

Optionally:
- [ ] Implement/reuse it for Concurrent Marking.

## JDK stuff

For build instructions please see the
[online documentation](https://openjdk.org/groups/build/doc/building.html),
or either of these files:

- [doc/building.html](doc/building.html) (html version)
- [doc/building.md](doc/building.md) (markdown version)

See <https://openjdk.org/> for more information about the OpenJDK
Community and the JDK and see <https://bugs.openjdk.org> for JDK issue
tracking.

More information about jdk22 can be found [here](https://openjdk.org/projects/jdk/22).
