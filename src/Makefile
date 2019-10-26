SUBDIRS = team-one team-two team-three
DIST = ./bin
SOURCES := $(shell find $(DIST) -name '*.o')

.PHONY: compile start clean

start:
	gcc $(SOURCES) -o main

compile:
	for dir in $(SUBDIRS); do \
        $(MAKE) -C $$dir ; \
		cp $$dir/$$dir.o ./bin; \
    done;

clean:
	for dir in $(SUBDIRS); do \
		rm -rf $$dir/$$dir.o; \
    done;\
	rm $(DIST)/*.o && rm ./main;

