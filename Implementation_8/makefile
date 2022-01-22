all: nbody4.g nbody4.i

nbody4.g: nbody4.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp
	
nbody4.i: nbody4.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp		
		
clean:
	rm -Rf *~ nbody4.g nbody4.i *.optrpt

