CXX = /usr/local/Cellar/gcc/7.2.0/bin/g++-7

all: 	bin/main.o ../../M2DO_FEA/bin/quadrature.o ../../M2DO_FEA/bin/linear_shape_function.o ../../M2DO_FEA/bin/node.o ../../M2DO_FEA/bin/solid_element.o ../../M2DO_FEA/bin/solid_material.o ../../M2DO_FEA/bin/mesh.o ../../M2DO_FEA/bin/boundary_conditions.o ../../M2DO_FEA/bin/sensitivity.o ../../M2DO_FEA/bin/stationary_study.o
		$(CXX) -std=c++14 -O3 -fopenmp -o bin/a.out bin/main.o ../../M2DO_FEA/bin/quadrature.o ../../M2DO_FEA/bin/linear_shape_function.o ../../M2DO_FEA/bin/node.o ../../M2DO_FEA/bin/solid_element.o ../../M2DO_FEA/bin/solid_material.o ../../M2DO_FEA/bin/mesh.o ../../M2DO_FEA/bin/boundary_conditions.o ../../M2DO_FEA/bin/sensitivity.o ../../M2DO_FEA/bin/stationary_study.o

bin/main.o: main.cpp
		$(CXX) -std=c++14 -O3 -w -c -o bin/main.o main.cpp -I ../../M2DO_FEA/include -I ../../M2DO_LSM/include -I ../../vendor/matvec/

../../M2DO_FEA/bin/quadrature.o: ../../M2DO_FEA/src/quadrature.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/quadrature.o ../../M2DO_FEA/src/quadrature.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/linear_shape_function.o: ../../M2DO_FEA/src/linear_shape_function.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/linear_shape_function.o ../../M2DO_FEA/src/linear_shape_function.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/node.o: ../../M2DO_FEA/src/node.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/node.o ../../M2DO_FEA/src/node.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/solid_element.o: ../../M2DO_FEA/src/solid_element.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/solid_element.o ../../M2DO_FEA/src/solid_element.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/solid_material.o: ../../M2DO_FEA/src/solid_material.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/solid_material.o ../../M2DO_FEA/src/solid_material.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/mesh.o: ../../M2DO_FEA/src/mesh.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/mesh.o ../../M2DO_FEA/src/mesh.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/boundary_conditions.o: ../../M2DO_FEA/src/boundary_conditions.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/boundary_conditions.o ../../M2DO_FEA/src/boundary_conditions.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/sensitivity.o: ../../M2DO_FEA/src/sensitivity.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/sensitivity.o ../../M2DO_FEA/src/sensitivity.cpp -I ../../M2DO_FEA/include

../../M2DO_FEA/bin/stationary_study.o: ../../M2DO_FEA/src/stationary_study.cpp
		$(CXX) -std=c++14 -O3 -w -c -o ../../M2DO_FEA/bin/stationary_study.o ../../M2DO_FEA/src/stationary_study.cpp -I ../../M2DO_FEA/include  

M2DO_FEA_clean:
	rm -rfv ../../M2DO_FEA/bin/*.o

clean:
	rm -rfv bin/*.out && rm -rfv results/area_fractions/* && rm -rfv results/level_set/* && rm -rfv results/boundary_segments/* && rm -rfv results/history/*
