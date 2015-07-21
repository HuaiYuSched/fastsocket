# Makefile for server

CC = gcc
CFLAGS = -Wall -g 
LDFLAGS = -pthread
USE_SSL = USE_SSL

ifdef USE_SSL
LDFLAGS +=  -g -lssl -lcrypto
CFLAGS += -D USE_SSL
endif

all: server

server: server.c server.h
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $<

clean:
	rm -rf server
