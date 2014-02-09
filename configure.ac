#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.65])
AC_INIT([xcluster], [10.0.2], [debathena@mit.edu])
AM_INIT_AUTOMAKE([foreign -Wall])
AM_MAINTAINER_MODE([enable])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_SRCDIR([xcluster.c])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CC

# Checks for libraries.
xcluster_save_LIBS=$LIBS
LIBS=
AC_CHECK_LIB([X11], [XGetDefault])
AC_CHECK_LIB([Xj], [XjUsage])
AC_SUBST([XJ_LIBS], $LIBS)
LIBS=
AC_CHECK_LIB([hesiod], [hesiod_init])
AC_SUBST([HESIOD_LIBS], $LIBS)
LIBS=$xcluster_save_LIBS

# Checks for header files.
AC_PATH_X
AC_SUBST([x_includes])
AC_SUBST([x_libraries])

AC_CHECK_HEADERS([fcntl.h netdb.h netinet/in.h stdlib.h string.h sys/param.h sys/socket.h sys/time.h])

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.
AC_FUNC_MALLOC
AC_CHECK_FUNCS([gethostbyname memset socket strrchr])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
