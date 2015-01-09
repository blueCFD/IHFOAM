Adaptation of IHFOAM to blueCFD-Core 2.3-1
==========================================

This adaptation has the necessary code changes for making IHFOAM build in blueCFD-Core 2.3-1. This version of blueCFD-Core has a port of OpenfOAM 2.3.x, commit `5f2583a17a53b0aeaa9849e177d4e357ff643470`, 18th of March 2014.

To use this port, run the following commands in the MSys terminal:
```
git clone https://github.com/blueCFD/IHFOAM.git

cd IHFOAM
git checkout blueCFD-Core-2.3-1

cd genAbs
./allMake > ../log.make 2>&1
cd ..

cd solvers/ihFoamOF230
./allMake >> ../../log.make 2>&1
```

If all goes well, this toolkit should now be build and ready to be used. The file `log.make` in the base folder `IHFOAM` will show you the full output from the build process, which will reveal if things will have gone well or not.

Note: This build has not yet been tested with IHFOAM's tutorial cases.


IHFOAM
======

IHFOAM is a set of solvers and boundary conditions to generate and absorb water waves actively at the boundaries and to simulate their interaction with porous coastal structures.

You can find all the information regarding the model at its web site:

http://ihfoam.ihcantabria.com/

The detailed instructions on how to download, compile and run the code can be found at:

http://openfoamwiki.net/index.php/Contrib/IHFOAM

Reference materials and test cases can be requested for free at:

http://ihfoam.ihcantabria.com/source-download/
