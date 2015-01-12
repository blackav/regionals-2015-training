### BEGIN ejudge auto-generated makefile ###
EJUDGE_PREFIX_DIR ?= /opt/ejudge
EJUDGE_CONTESTS_HOME_DIR ?= /home/judges
EJUDGE_LOCAL_DIR ?= /var/lib/ejudge
EJUDGE_SERVER_BIN_PATH ?= /opt/ejudge/libexec/ejudge/bin

CXX = g++
CXXFLAGS = -Wall -g -O2
CXXLIBCHECKERFLAGS = -m32 -Wall -g -O2 -I${EJUDGE_PREFIX_DIR}/include/ejudge -L${EJUDGE_PREFIX_DIR}/lib -Wl,--rpath,${EJUDGE_PREFIX_DIR}/lib
CXXLIBCHECKERLIBS = -lchecker -lm

EXECUTE = ${EJUDGE_PREFIX_DIR}/bin/ejudge-execute
EXECUTE_FLAGS =  --input-file=sweets.in --output-file=sweets.out --test-pattern=%02d --corr-pattern=%02d.a --time-limit=2

NORMALIZE = ${EJUDGE_SERVER_BIN_PATH}/ej-normalize
NORMALIZE_FLAGS = --workdir=tests --test-pattern=%02d --corr-pattern=%02d.a

all : check
check_settings : all normalize


check : check.cpp
	${CXX} -DEJUDGE ${CXXLIBCHECKERFLAGS} check.cpp -ocheck ${CXXLIBCHECKERLIBS}


normalize :
	${NORMALIZE} ${NORMALIZE_FLAGS} --all-tests

clean :
	-rm -f *.o *.class *.exe *~ *.bak check

### END ejudge auto-generated makefile ###
