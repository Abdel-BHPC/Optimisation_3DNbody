all:  nbody3.g nbody3.i 

nbody3.g: nbody3.c	
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp
	
nbody3.i: nbody3.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp
	
clean:
	rm -Rf *~  nbody3.g nbody3.i *.optrpt

