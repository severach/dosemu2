top_builddir=../../..
include ../plugins.mak
$(eval $(makefile_conf))

# This is the Makefile for the debugger-subdirectory of DOSEMU.
# Please send comments and bug-reports to Max Parke <mhp@light.lightlink.com>
# Please read the code in this directory for more information.


#The C files, include files and dependancies here.
CFILES = mhpdbg.c mhpdbgc.c dis8086.c dosdebug.c
DEPENDS =  mhpdbg.d mhpdbgc.d dis8086.d dosdebug.d
HFILES =

# Insert all source- and header-files here.
ALL = $(CFILES) $(HFILES) README.dosdebug README.recover Changelog

# All object-files are included here.
OBJS =  mhpdbg.o mhpdbgc.o dis8086.o

all: lib $(BINPATH)/bin/dosdebug

dosdebug: dosdebug.c
	$(CC) $(ALL_CFLAGS) $(ALL_CPPFLAGS) $(DOSDEBUG_DEFS) $< $(ALL_LDFLAGS) $(DOSDEBUG_LIBS) -o $@

$(BINPATH)/bin/dosdebug: dosdebug | $(BINPATH)/bin
	cp $< $@

install:

clean::
	rm -f dosdebug

include $(REALTOPDIR)/src/Makefile.common
