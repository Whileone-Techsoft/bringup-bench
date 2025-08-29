PREF=/proj/perf/data/compilers/release-20240927-centos7/riscv64-unknown-linux-gnu/bin/riscv64-unknown-linux-gnu-
CXX = ${PREF}g++
SPIKE_DIR = ../../../riscv-isa-sim/

CFLAGS = -Wall -Werror -g -I $(SPIKE_DIR) 

build: simple_mmio_plugin.so

simple_mmio_plugin.so: simple_mmio_plugin.cpp
	$(CXX) -shared -o simple_mmio_plugin.so $(CFLAGS) -fPIC simple_mmio_plugin.cpp

clean:
	-rm -f *.o simple_mmio_plugin.so
