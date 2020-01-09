CC = g++
CFLAGS = -Wall -ansi -pedantic
OBJS = employee.o address.o main.o
EXEC = myProgram
MANIFEST = *.cpp *.h Makefile
DESTDIR = $(HOME)/bin
VER = 0.1

all: $(EXEC)
$(EXEC): $(OBJS)
		$(CC) -o $@ $+ 
%.o: %.cpp
		$(CC) -c  $<

main.o: employee.h address.h
employee.o: address.h

clean:
		rm -f *~ rm -f *.bak rm -f $(EXEC) $(OBJS)
install: all
		sh -c "if [ ! -d $(DESTDIR) ] ; then mkdir $(DESTDIR) ; fi"
		cp $(EXEC) $(DESTDIR)/$(EXEC)
		echo hello: zainstalowane!
dist: clean
		tar cvzf ../$(EXEC)-$(VER).tar.gz $(MANIFEST)
.PHONY:
		clean
