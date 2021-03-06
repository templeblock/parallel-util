# parallel-util

Simple implementation of "parallel_for" using C++11

## Usage

Suppose that you have a process expressed using C++11 lambda expressions:
```
auto process = [](int i) { ... };
```
and want to parallelize the following for loop:
```
for (int i = 0; i < n; ++ i) { process(i); }
```
This can be easily parallelized by
```
parallelutil::parallel_for(n, process);
```
This is based on multi-threading and the default concurrency is set to the hardware concurrency.

## Installation

`parallel-util` is a header-only, single-file library. It can be used by just copying `parallel-util.hpp` and pasting it into your project.

Alternatively, it can be installed using `cmake`. If your project is also managed using `cmake`, `ExternalProject` commands are useful for including `parallel-util` to your project.

## Persuing Further Performance

Please consider to use other complex libraries such as Intel(R) Threading Building Blocks.

## Projects using parallel-util

- Sequential Line Search <https://github.com/yuki-koyama/sequential-line-search>
- OptiMo <https://github.com/yuki-koyama/optimo>
- SelPh <https://github.com/yuki-koyama/selph>

## LICENSING

MIT License.
