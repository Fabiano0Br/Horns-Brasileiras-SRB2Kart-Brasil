#convertpk3 Makefile by F.A Paulino (filpAM)

CXX = g++
CC = gcc

CXXFLAGS = -std=c++17 -lstdc++fs
CFLAGS = -std=c99

LIBS =  -lz

CXX_OBJ = convert.o main.o
C_OBJ = wad.o lzf_d.o lzf_c.o zip.o ioapi.o

OBJ_FILES += $(CXX_OBJ)
OBJ_FILES += $(C_OBJ)

.PHONY : all clean
all: convertpk3

clean:; rm *.o

convertpk3: $(OBJ_FILES)
	$(CXX) $(CXXFLAGS) $(OBJ_FILES) $(LIBS) -o convertpk3


$(CXX_OBJ): %.o: %.cpp
	$(CXX) -c $(CXXFLAGS) -o $@ $<

$(C_OBJ): %.o: %.c
	$(CC) -c $(CFLAGS) -o $@ $<



