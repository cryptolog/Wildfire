Wildfire integration/staging tree
================================

http://alchemists-guild.dx.am/

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2018 Wildfire Developers

Where to get the Client?
-----------------------

https://github.com/Alchemists-Guild/WildfireClient

What is Wildfire?
----------------

Wildfire is a faster version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 30 second block targets
 - subsidy halves in 4200000 blocks (~4 years)
 - 35 billion total coins
 - 5000 coins per block
 - 10 blocks to retarget difficulty

The rest is the same as Bitcoin.

License
-------

Wildfire is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Wildfire
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable.

Testing
-------

Testing and code review is the bottleneck for development. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake WILDFIRE_QT_TEST=1 -o Makefile.test wildfire-qt.pro
    make -f Makefile.test
    ./wildfire-qt_test
