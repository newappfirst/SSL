# Generated automatically from Makefile.in by configure.
CC=gcc
CFLAGS=-g -I/usr/include  -Wall 
LD=-L/usr/lib/x86_64-linux-gnu/  -lssl -lcrypto
DISTDIR=openssl-examples-20010815
DISTFILE=${DISTDIR}.tar.gz

DIST=	client.c \
	client.h \
	common.c \
	common.h \
	server.c \
	server.h \
	wserver.c \
	wserver2.c \
	read_write.c \
	read_write.h \
	sclient.c \
	wclient.c \
	wclient2.c \
	Makefile.in \
	configure.in \
	configure \
	client.pem \
	server.pem \
	root.pem \
	dh1024.pem \
	README \
	RUNNING 

OBJS=common.o 

all:  wclient wserver wclient2 wserver2 sclient

sclient: sclient.o client.o read_write.o $(OBJS)
	$(CC) sclient.o client.o read_write.o $(OBJS) -o sclient $(LD)

wclient: wclient.o client.o  $(OBJS)
	$(CC) wclient.o client.o $(OBJS) -o wclient $(LD)

wclient2: wclient2.o client.o  $(OBJS)
	$(CC) wclient2.o client.o $(OBJS) -o wclient2 $(LD)

wserver: server.o wserver.o  $(OBJS)
	$(CC) wserver.o server.o $(OBJS) -o wserver $(LD)

wserver2: server.o wserver2.o $(OBJS)
	$(CC) wserver2.o server.o $(OBJS) -o wserver2 $(LD)

clean:	
	rm -rf *.o wclient wserver wclient2 wserver2 sclient
dist:
	rm -rf ${DISTDIR}; mkdir ${DISTDIR}
	cp ${DIST} ${DISTDIR}
	rm -f ${DISTFILE}
	tar cf - ${DISTDIR} | gzip > ${DISTFILE}
