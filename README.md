# Boolean Expressions

[![Build Status](https://travis-ci.org/cjdrake/boolexpr.svg?branch=master)](https://travis-ci.org/cjdrake/boolexpr)

BoolExpr is a C++ library for symbolic Boolean algebra.

[Read the docs!][boolexpr]

## System Dependencies

This code is known to compile on Ubuntu Trusty Linux.
Install the following dependencies:

    sudo apt-get install -y build-essential cmake doxygen

## Getting Started

To get started using the code,
first clone the repository and its `third_party` dependencies:

    git clone --recursive https://github.com/cjdrake/boolexpr
    cd boolexpr

Create a local build directory, and run `cmake`:

    mkdir build
    cd build
    cmake -DCMAKE_BUILD_TYPE=Coverage ..
    make

## Run Tests

After the dependencies have been built,
to run the functional test suite::

    make do_test

To collect code coverage data::

    make cover

The coverage report will be in `build/html/index.html`.

## Build Documentation

The documentation uses [Doxygen][doxygen] and [Sphinx][sphinx].
To build the html version:

    pip install sphinx
    make pyhtml

The documentation will be in `build/python/build/sphinx/html/index.html`.

## Contributing

If you have some idea you would like to see realized,
please email me.

[boolexpr]: http://www.boolexpr.org
[doxygen]: http://www.doxygen.org
[sphinx]: http://www.sphinx-doc.org
