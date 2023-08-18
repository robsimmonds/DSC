Bootstrap: docker
From: ubuntu

%files

%post
	apt update
	apt -y upgrade

DEBIAN_FRONTEND="noninteractive" apt install -y apt-utils git cmake g++ libhdf5-dev libcfitsio-dev pkgconf
	git clone https://github.com/CARTAvis/fits2idia
 	cd fits2idia
 	mkdir build
 	cd build
 	cmake ..
 	make
	cp fits2idia /usr/local/bin

%runscript
	/usr/local/bin/fits2idia "$@"

