# Memory Manager

A C++ implementation of an operating-system-style memory manager that tracks dynamic heap
allocation. The standard `malloc`/`free` are reimplemented here as `claimMemory` and
`freeMemory`, satisfying a set of allocation/deallocation requirements. Completed during
an Erasmus semester at Fontys University of Applied Sciences (Netherlands).

> *In this assignment we implement a Memory Manager used by an operating system to keep
> track of dynamic memory allocation (allocation from the heap). The equivalents of
> "malloc/free" are `claimMemory` and `freeMemory`; my task was to implement these and
> meet every requirement in the process.*

**Tech stack:** C++ · Make · GoogleTest / GoogleMock

## Features

- Custom heap allocator with `claimMemory` / `freeMemory` semantics.
- Internal free/used block tracking via a managed list (`MList`).
- Test-driven: a GoogleTest/GoogleMock suite validates the allocation requirements.

## Project structure

```
├── main.cpp
├── product/   MList.{h,cpp}, testUi.{h,cpp}    # allocator + manual test UI
└── test/      mytests.cpp                       # GoogleTest/GoogleMock suite
```

## Build & test

```bash
make            # build the memory manager
make test       # build & run the GoogleTest suite (requires gtest/gmock)
```

---

*Fontys (Erasmus) coursework. A systems-programming exercise in manual memory management,
built test-first in C++.*
