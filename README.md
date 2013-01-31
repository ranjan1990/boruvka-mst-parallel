boruvka-mst-parallel
====================

--------------------------
Folder(s)/File(s) included
--------------------------
OpenCL  Tutorial.pdf	OpenCL Installation Guide.

CL			Includes all the header files for OpenCL. While following
			  OpenCL Installation Guide, skip step #6 and just run the
			  the command,
			  sudo cp /path-to-CL-folder /usr/include/
			  (Note: You need to specify a valid path where CL folder reside)

code		This folder includes sequential and parallel code.

code/sequential/mst.cpp   Implementation of sequential program

code/parallel/CL          It's a local copy of the similar CL folder mentioned above.

code/parallel/pmst.cpp    Implentation of parallel program

-------------------------------
Commands to run Sequential Code
-------------------------------
1. g++ mst.cpp -o mst
2. ./mst

---------------------------
Commands to run OpenCL Code
---------------------------
#1 g++ -c -Wall -I /usr/include/CL/ filename.cpp -o filename.o
#2 g++ filename.o -o filename -L /usr/lib/OpenCL/ -l OpenCL   (for 32-bit)
   g++ filename.o -o filename -L /usr/lib64/OpenCL/ -l OpenCL (for 64-bit)
#3 ./filename
