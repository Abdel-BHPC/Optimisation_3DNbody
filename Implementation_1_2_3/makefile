all:  nbody1.g  nbody1.i 

nbody1.g: nbody1.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp	

nbody1.i: nbody1.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp	
		
clean:
	rm -Rf *~  nbody1.g  nbody1.i *.optrpt

