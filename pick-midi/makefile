CC=gcc

SRCDIR := src
OUTDIR := bin
CFLAGS := -c -Wall
LDFLAGS := -lm -lfftw3
SOURCES := $(wildcard $(SRCDIR)/*.c)
OBJECTS := $(patsubst %.c,%.o,$(SOURCES))
EXECUTABLE := pick-midi

all: $(SOURCES) $(EXECUTABLE)
	
$(EXECUTABLE): $(OUTDIR) $(OBJECTS) 
	$(CC) -o $(OUTDIR)/$@ $(OBJECTS) $(LDFLAGS) 
	rm $(OBJECTS)
	
$(OUTDIR):
	mkdir $(OUTDIR)

.o:
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -rf $(OUTDIR)
