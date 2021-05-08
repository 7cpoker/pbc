CC = gcc
CFLAGS = -O2 -fPIC -Wall
LUADIR = ../../../../skynet/3rd/lua
TARGET = ../../../../qcclib/protobuf.so
SHARED = -shared #for Linux
#SHARED= -bundle -undefined dynamic_lookup #for MacOS X

.PHONY : all clean

all : $(TARGET)

$(TARGET) : pbc-lua53.c
	$(CC) $(CFLAGS) $(SHARED) -o $@ -I../.. -I$(LUADIR) -L../../build $^ -lpbc

clean :
	rm -f $(TARGET)
