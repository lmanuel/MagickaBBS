# type either "make linux", "make win32", or "make os2" to compile

help:
	@echo You can use this Makefile in the following ways:
	@echo gmake freebsd ......... Make FreeBSD binaries
	@echo make linux ............ Make Linux binaries
	@echo gmake cleanfreebsd .... Remove object files under FreeBSD
	@echo make cleanlinux ....... Remove object files under Linux

freebsd :
	mkdir -p bin
	gmake -C src -f Makefile freebsd

linux :
	mkdir -p bin
	make -C src -f Makefile linux

cleanfreebsd :
	rm -rf bin
	gmake -C src -f Makefile cleanfreebsd

cleanlinux :
	rm -rf bin
	make -C src -f Makefile cleanlinux

