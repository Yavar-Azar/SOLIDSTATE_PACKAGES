# SOLIDSTATE_PACKAGES



## FHI_aims



### Installation

- extract fhi-aims.tar,gz

- cd  to fhi home direcory

- mkdir build

- cd build

- edit your own cmake file (for example openmpi.intel.cmake)

  ```cmake
  set(TARGET_NAME aims.x CACHE STRING "")
  set(CMAKE_INSTALL_PREFIX "$ENV{AIMS_HOME}" CACHE STRING "")
  
  ###############
  # Basic Flags #
  ###############
  set(CMAKE_Fortran_COMPILER /home/yavar/SOURCES/OMP412/bin/mpif90 CACHE STRING "")
  set(CMAKE_Fortran_FLAGS "-O3 -ip -fp-model precise" CACHE STRING "")
  set(Fortran_MIN_FLAGS "-O0 -fp-model precise" CACHE STRING "")
  set(LIB_PATHS "/home/yavar/intel/compilers_and_libraries_2020.4.304/linux/mkl/lib/intel64" CACHE STRING "")
  set(LIBS "mkl_scalapack_lp64 mkl_blacs_openmpi_lp64 mkl_intel_lp64 mkl_sequential mkl_core" CACHE STRING "")
  
  ###############
  # C,C++ Flags #
  ###############
  set(CMAKE_C_COMPILER icc CACHE STRING "")
  set(CMAKE_C_FLAGS "-O3 -ip -fp-model precise -std=gnu99" CACHE STRING "")
  
  ```

  

- create cmake file 

  ```sh
  cmake -C open_mpi.intel.cmake ..
  ```



- make -j  4



## Quantum ESPRESSO

