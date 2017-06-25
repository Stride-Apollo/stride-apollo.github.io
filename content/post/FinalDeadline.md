+++
date = "2017-06-25T23:09:56+01:00"
title = "Final deadline"
+++

The Apollo project is done.

<!--more-->

After 5-6 months, it's over.
We've implemented the following features:

- A visualization tool with lots of graphs.
- Multi region shared memory.
- HDF5 checkpointing (works with Multi region).
- A generator of synthetic populations (whose performance was drastically improved during the project).
- A library for multithreaded programming, giving the user the choice to use TBB or OpenMP.

However, we've failed to implement some features:

- Multi region MPI: We were very close to a solution. The reason this part is delayed, is because MPI consists of very old C code.
- The performance report concerning multithreading: We gave Multi region MPI priority over this.
- Paraview: Due to the inability to compile Paraview, we couldn't work on this feature.

We hope our efforts will help the Stride project in its future endeavours.

Sincerely, The Apollo Team
