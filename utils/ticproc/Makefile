OS := $(shell uname -s)

ifeq ($(OS), FreeBSD)
  CC=cc
  CFLAGS=-I/usr/local/include
  LDFLAGS=-L/usr/local/lib
endif
ifeq ($(OS), NetBSD)
  CC=cc
  CFLAGS=-I/usr/pkg/include
  LDFLAGS=-L/usr/pkg/lib
endif
ifeq ($(OS), Linux)
  CC=gcc
  CFLAGS=
  LDFLAGS=
endif
ifeq ($(OS), Darwin)
  CC=cc
  CFLAGS=
  LDFLAGS=
endif


DEPS = ticproc.c

OBJ = ticproc.o ../../inih/ini.o crc32.o
%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)


ticproc: $(OBJ)
	$(CC) -o ticproc -o $@ $^ $(CFLAGS) $(LDFLAGS) -lsqlite3

.PHONY: clean

clean:
	rm -f $(OBJ) ticproc
