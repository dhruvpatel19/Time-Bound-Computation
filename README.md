# Time-Bound-Computation

A common library utilized when perfoming vector-based operations such as matrix multiplication is numpy, and a question that gets asked frequently is: Why is numpy faster than a pure python solution to the given problem? One of the primary reasons is that numpy is wrapped in C (data is compiled during execution and operations are optimized) and simply implemented as a module in Python, while pure Python itself has the additional component of being interpreted - making decisions on what the operation is stating, and then conducting the operation. In more technical terms, numpy operates through dense, homogenous arrays, which allows for a better locality of reference. This, in turn, avoids the general cost of looping that Python contains, and prevents pointer indirection and per-element dynamic checking, both characteristics of Python lists (as Python lists are arrays of pointers to objects).

However, numpy has some drawbacks - it works significantly slower than Python for scalar/non-vectorized operations, and it also only provides a significant reduction in execution time across large pieces of data or data that is typically more complicated to analyze (like an NxN matrix). Thus, in this particular case, numpy works significantly better than python, but for elementary operations, Python would be the faster option.
