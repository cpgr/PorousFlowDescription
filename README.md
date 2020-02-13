# PorousFlow

The PorousFlow module of MOOSE enables the simulation of flow and transport through porous media

## Use

PorousFlow documentation can be found at https://mooseframework.org/modules/porous_flow/index.html, which describes:

- the physics
- examples and a tutorial
- details concerning the test suite
- implementation details

New PorousFlow users who have never used MOOSE before are encouraged to check-out its
[tutorial](https://mooseframework.org/workshop/) and [examples](https://mooseframework.org/examples/index.html).

Doxygen pages for PorousFlow are at https://mooseframework.org/docs/doxygen/modules/classes.html

## License

PorousFlow is distributed with MOOSE under the [Gnu Lesser General Public License](https://github.com/idaholab/moose/blob/master/LICENSE)

## Install

PorousFlow comes packaged with the MOOSE framework.  To install MOOSE and PorousFlow, please follow the instructions at https://mooseframework.inl.gov/getting_started/index.html.  After building and testing MOOSE you will need to build PorousFlow, which is an easy step:
``
cd <path_to_moose>/modules/porous_flow
make
``
You may optionally use `make -j8` if your system has 8 available cores (or `-j4` if it has 4, etc).


## Testing

PorousFlow comes with hundreds of tests.  To ensure it is running correctly:
``
cd <path_to_moose>/modules/porous_flow
./run_tests
``
You may optionally use `./run_tests -j8` if your system has 8 available cores (or `-j4` if it has 4, etc).

## Contributing

You are free to contribute to PorousFlow, and the process is described [here](https://mooseframework.inl.gov/framework_development/contributing.html).  MOOSE has strict quality control standards.

## Contact

Please contact the main MOOSE discussion list moose-users@googlegroups.com.  A PorousFlow developer will answer your question.
