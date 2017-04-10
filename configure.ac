#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([sunagl], [1.0], [dev001hajipro@gmail.com])
AM_INIT_AUTOMAKE([foreign])
AC_CONFIG_SRCDIR([src/sunagl.c])
AC_CONFIG_HEADERS([config.h])


# Checks for programs.
AC_PROG_CC

# has system pkg-config?
PKG_PROG_PKG_CONFIG


PKG_CHECK_MODULES([GL], [gl], [have_gl=yes], [have_gl=no])
PKG_CHECK_MODULES([GLU], [glu], [have_glu=yes], [have_glu=no])
if test x$have_glu != xno; then
  AC_MSG_NOTICE([glu : $have_glu])
  AC_DEFINE(HAVE_LIBGLU, 1, [wheter GL/glu is available])
else
  AC_MSG_ERROR(X11/glu is not available.)
fi
AC_SUBST(GLU_CFLAGS)
AC_SUBST(GLU_LIBS)

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADER([GL/gl.h],, AC_MSG_ERROR([gl.h not found]))
AC_CHECK_HEADER([GL/glu.h],, AC_MSG_ERROR([glu.h not found]))

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_CONFIG_FILES([Makefile
                 src/Makefile])
AC_OUTPUT
