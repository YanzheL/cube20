# Cube 20 Project

Sources for Coset Solver and Two-Phase Solver

The original source code from [Cube20 Source](https://www.cube20.org/src) is written in [CWeb](https://www-cs-faculty.stanford.edu/~knuth/cweb.html) format, which is not very convenient for developers, so I converted it to an easy-to-build C++ project. Fork it as you like.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Provided that you have cmake, g++, git in your linux-like system, if you do not have them, run:

```
apt-get install cmake g++ git
```

### Compiling

Clone this repo and enter the directory

```shell
git clone https://github.com/YanzheL/cube20.git && cd cube20
```

Build the libraries and executables

```bash
mkdir build && cd build
cmake ..
make
```

## Running the tests

[Instructions on running twophase](https://www.cube20.org/src/twophase.html)

[Instructions on running hcoset.](https://www.cube20.org/src/hcoset.html)

## Author

* **[Tomas Rokicki](https://github.com/rokicki)** - *Initial work* - [Cube20 Source](https://github.com/rokicki/cube20src)

## Acknowledgments

* [Cube20 Project](https://www.cube20.org)