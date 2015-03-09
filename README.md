# pikaia [![GitHub release](https://img.shields.io/github/release/jacobwilliams/pikaia.svg?style=plastic)](https://github.com/jacobwilliams/pikaia/releases/latest)
Modern Fortran Edition of the Pikaia Genetic Algorithm 

Overview
------

This is an refactoring of the PIKAIA unconstrained optimization code from the [High Altitude Observatory](http://www.hao.ucar.edu/modeling/pikaia/pikaia.php).  The original code is public domain and was written by Paul Charbonneau & Barry Knapp.  The new code differs from the old code in the following respects:
 * The original fixed-form source (FORTRAN 77) was converted to free-form source.
 * The code is now object-oriented Fortran 2003/2008.  All user interaction is now through the ```pikaia_class```.
 * All real variables are now double precision.
 * The random number generator was replaced with calls to the intrinsic Fortran ```random_number``` function.
 * There are various new options (e.g., a convergence window with a tolerance can be specified as a stopping condition, and the user can specify a subroutine for reporting iterations).
 * Mapping the variables to be between 0 and 1 now occurs internally, rather than requiring the user to do it.
 * Can now include an initial guess in the initial population.

Compiling
------

A build script, `build.sh` is provided in the project root directory. This script uses [FoBiS](https://github.com/szaghi/FoBiS) to build the pikaia library and an example program.

Examples
------

Coming soon...

Documentation
--------------

 * The API documentation can be generated by processing the source files with [RoboDoc](http://rfsber.home.xs4all.nl/Robo/).  Note that the shell script will also generate these files automatically in the ```documentation``` folder, assuming you have RoboDoc installed.
 * The original Pikaia documentation (for v1.2) can be found [here](http://www.hao.ucar.edu/modeling/pikaia/relnotes.ps).

See also
------
 * PIKAIA description page: http://www.hao.ucar.edu/modeling/pikaia/pikaia.php
 * Original source code: http://download.hao.ucar.edu/archive/pikaia/

