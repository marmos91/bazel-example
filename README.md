# Bazel example

A basic bazel build example repository for C++ projects

## How to build

```bash
bazel build //main:hello-world
```

## How to generate dependency graph

Note: you have to install [xdot](https://github.com/jrfonseca/xdot.py) and [graphviz](https://www.graphviz.org/)

```bash
xdot <(bazel query --nohost_deps --noimplicit_deps 'deps(//main:hello-world)' --output graph)
```
