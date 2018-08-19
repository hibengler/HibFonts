AC_INIT([hibfonts],[0.1],[h@killercool.net])

# For libtool.
dnl Please update these for releases.
OPUS_LT_CURRENT=5
OPUS_LT_REVISION=0
OPUS_LT_AGE=5

AC_CONFIG_SRCDIR(src/FTPoint.cpp)
AC_CONFIG_AUX_DIR(.auto)


AM_INIT_AUTOMAKE([1.6 no-define subdir-objects ])
AM_CONFIG_HEADER(config.h)

AC_CONFIG_FILES([Makefile])

AC_PROG_CC

LT_MAJOR="0"
LT_MINOR="1"
LT_MICRO="2"
AC_SUBST(LT_MAJOR)
AC_SUBST(LT_MINOR)
AC_SUBST(LT_MICRO)
LT_VERSION="$LT_MAJOR:$LT_MINOR:$LT_MICRO"
AC_SUBST(LT_VERSION)

AC_PROG_LIBTOOL
AC_PROG_INSTALL


AC_HEADER_STDC
AC_CHECK_HEADER([stdlib.h])

AC_PATH_X



dnl Check for OpenGL ES2 
AC_MSG_CHECKING(for OpenGL ES2 support) 
have_opengles2=no 
AC_TRY_COMPILE([  
#if defined (__IPHONEOS__)     
#include <OpenGLES/ES2/gl.h>     
#include <OpenGLES/ES2/glext.h>  
#else     
#include <GLES2/gl2.h>     
#include <GLES2/gl2ext.h>  
#endif 
],[ 
],[ 
have_opengles2=yes 
]) 
AC_MSG_RESULT($have_opengles2) 
GLLIB="" 
GLES2LIB="" 
if test x$have_opengles2 = xyes; then     
  CFLAGS="$CFLAGS -DHAVE_OPENGLES2"     
  #GLES2LIB="$XPATH -lGLESv2" 
fi 
if test x$have_opengl = xyes; then  
   CFLAGS="$CFLAGS -DHAVE_OPENGL"     
   GLLIB="$XPATH $SYS_GL_LIBS"
fi
 
AC_SUBST(GLLIB) AC_SUBST(GLES2LIB) AC_SUBST(XLIB) 




AC_OUTPUT
