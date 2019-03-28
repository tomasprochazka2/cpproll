# TOTO NENI KONECNE RESENI
# Finalne bude slozka debian/* a bude se delat balik
# Vsechny dependencies jsou napsane pro kompilaci v pbuilderu

all: deps

spdlog:
	apt-get -y install git ca-certificates
	git clone https://github.com/gabime/spdlog.git
	#apt-get -y install libspdlog-dev # zpusobuje asi chybu v clippu

boost-bloom-filters:
	git clone https://github.com/queertypes/boost-bloom-filters.git

clipp:
	git clone https://github.com/muellan/clipp.git

# osklive, potreba ubalit a dat do zavislosti:

liblbfgs:
	# git clone https://github.com/chokkan/liblbfgs.git
	# cd liblbfgs; \
    # ./autogen.sh; \
    # ./configure
	# .$(MAKE) -C liblbfgs
	# selze autogen, proto radeji instalovat balik
	apt-get install -y liblbfgs-dev

eigen3:
	apt-get install -y libeigen3-dev

boostlibs:
	apt-get install -y libboost-iostreams-dev libboost-serialization-dev liblbfgs-dev

cmake:
	apt-get install -y cmake


deps: spdlog boost-bloom-filters clipp liblbfgs eigen3 boostlibs cmake

