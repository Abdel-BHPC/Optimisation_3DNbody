all: nbody.g nbody1.g nbody2.g nbody3.g nbody4.g nbody.i nbody1.i nbody2.i nbody3.i nbody4.i

nbody.g: nbody.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp
	
nbody1.g: nbody1.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp	

nbody2.g: nbody2.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp

nbody3.g: nbody3.c	
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp
	
nbody4.g: nbody4.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp
	
nbody.i: nbody.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp
	
nbody1.i: nbody1.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp	

nbody2.i: nbody2.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp
	
nbody3.i: nbody3.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp
	
nbody4.i: nbody4.c
	icc -xhost -Ofast -fp-model fast=2 -qopt-report $< -o $@ -qmkl -qopenmp		
		
clean:
	rm -Rf *~ nbody.g nbody1.g nbody2.g nbody3.g nbody4.g nbody.i nbody1.i nbody2.i nbody3.i nbody4.i *.optrpt

