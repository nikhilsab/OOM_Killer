.PHONY: all clean

CC = gcc
INCLUDES = -I .
TARGET = PSI_Mem
MAP_FILE = PSI_Mem.map

CC_OPTIONS = -Wall -O2 -g
LD_FLAGS = -Xlinker -Map=$(MAP_FILE)

OBJ_FILES = PSI_Mem.c

.SILENT: clean all %.o

all: ${OBJ_FILES}
	@echo "Building ${TARGET} ..."
	${CC} ${CC_OPTIONS} ${LD_FLAGS} ${OBJ_FILES} -o ${TARGET}

%.o: %.c
	@echo "Compiling $*.o ..."
	${CC} ${CC_OPTIONS} $(LD_FLAGS) -c $*.c ${INCLUDES}

clean:
	@echo "Cleaning $(OBJ_FILES) $(TARGET) $(MAP_FILE)..."
	-rm -rf	 *.o
	-rm -rf	 PSI_Mem.map
	-rm -rf	 PSI_Mem
