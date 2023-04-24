PROJ=/home/udit/multichat_2
BIN=$(PROJ)/bin
SERVER=$(PROJ)/server
CLIENT=$(PROJ)/client
COMMON=$(PROJ)/common
CC=g++
CPPFLAGS=-g -Wall -std=c++11 -I$(COMMON)
LFLAGS=-lpthread
SERVER_OBJS=$(SERVER)/server.o
CLIENT_OBJS=$(CLIENT)/client.o

all : $(BIN)/server $(BIN)/client $(COMMON_OBJS)

$(BIN)/server : $(SERVER_OBJS) $(COMMON_OBJS)
	$(CC) $^ -o $@ $(LFLAGS)

$(BIN)/client : $(CLIENT_OBJS) $(COMMON_OBJS)
	$(CC) $^ -o $@ $(LFLAGS)

%.o : %.c
	$(CC) -c $(CPPFLAGS) $< -o $@

clean:
	\rm -f $(BIN)/server $(BIN)/client
	\rm `find $(PROJ) -name '*.o'`


