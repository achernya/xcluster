bin_PROGRAMS = xcluster cview

xcluster_SOURCES = \
	check.c \
	mit-copyright.h \
	net.c \
	net.h \
	points.h\
	read.c \
	xcluster.c \
	xcluster.h

xcluster_LDADD = @x_libraries@ @XJ_LIBS@ @HESIOD_LIBS@

cview_SOURCES = \
	cview.c \
	net.c \
	net.h 
cview_LDADD = @HESIOD_LIBS@

dist_man1_MANS = \
	xcluster.1 \
	cview.1

appdefsdir=${sysconfdir}/X11/app-defaults
appdefs_DATA = Xcluster
EXTRA_DIST = Xcluster
