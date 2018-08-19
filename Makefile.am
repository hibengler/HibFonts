AUTOMAKE_OPTIONS = foreign

bin_PROGRAMS = hibfont hibfont_static

pkglib_PROGRAMS = hibfont


hibfont_SOURCES = hibfont.c
hibfont_LDADD = libhibfont.la

hibfont_static_SOURCES = hibfont.c
hibfont_static_LDADD = libhibfont.la
hibfont_static_LDFLAGS = -static


# Build a libtool library, libhello.la for installation in libdir.
lib_LTLIBRARIES = libhibfont.la
libhello_la_SOURCES = letters.c letters_ascii.c letters_render_opengles2.c letters_ascii.h letters.h letters_render_opengles2.h
libhello_la_LDFLAGS = -version-info 1:8:1
