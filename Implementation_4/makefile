all:  nbody2.g  nbody2.i 

nbody2.g: nbody2.c
	gcc -march=native -mavx2 -Ofast -fopt-info-all=nbody.gcc.optrpt $< -o $@ -lm -fopenmp

nbody2.i: nbody2.c
	icc -xhost -Ofast -qopt-report $< -o $@ -qmkl -qopenmp	
		
clean:
	rm -Rf *~ nbody2.g nbody2.i  *.optrpt

