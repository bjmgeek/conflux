[![Build Status](https://travis-ci.org/cmars/conflux.svg?branch=master)](https://travis-ci.org/cmars/conflux)

conflux - Distributed database synchronization
==============================================

Conflux synchronizes data by unique content-addressable identifiers.
It does this by representing the entire set of identifiers with a
polynomial. The difference between the databases is represented as
a ratio of these polynomials. However, the polynomials are very large,
since they represent every identifier in the database. The difference
between databases is communicated by evaluating the difference ratio
at a number of constants. Through the magic of rational function
interpolation, the difference ratio can be reconstructed from these
data points.

This algorithm is described in the papers, ["Set Reconciliation with 
Nearly Optimal Communication Complexity"](http://ipsit.bu.edu/documents/ieee-it3-web.pdf) and 
["Practical Set Reconciliation"](http://ipsit.bu.edu/documents/BUTR2002-01.ps).

The reconciliation algorithm are released under the GNU General Public License version 3.
The reconciliation network protocol and prefix tree data storage interfaces
are released under the Affero General Public License version 3.

Copyright (C) 2012,2013  Casey Marshall <casey.marshall@gmail.com>
