## Makefile.am for the NEWGAL library

AM_CPPFLAGS = -I$(abs_top_srcdir)/src/include -I$(abs_top_srcdir)/include $(PIXMAN_CFLAGS)

noinst_LTLIBRARIES = libnewgal.la

# Define which subdirectories need to be built
SUBDIRS = @VIDEO_SUBDIRS@
DIST_SUBDIRS = dummy fbcon qvfb wvfb em85xxyuv em85xxosd svpxxosd bf533 utpmc \
               mb93493 commlcd shadow mlshadow dfb em86gfx hisi rtos_xvfb pcxvfb \
               nexus s3c6410 sigma8654 mstar gdl stgfb usvfb drm
# x11 dga vgl svga ggi aalib

EXTRA_DIST=makefile.ng makefile.msvc

DRIVERS = @VIDEO_DRIVERS@

# Include the architecture-independent sources
COMMON_SRCS =       \
    video.c         \
    newgal.c        \
    surface.c       \
    RLEaccel.c      \
    RLEaccel_c.h    \
    blit.c          \
    blit.h          \
    blit_0.c        \
    blit_1.c        \
    blit_A.c        \
    blit_A.h        \
    blit_N.c        \
    leaks.h         \
    pixels.c        \
    pixels_c.h      \
    stretch.c       \
    stretch_c.h     \
    sysvideo.h      \
    videomem-bucket.h   \
    videomem-bucket.c   \
    surface-shared.c    \
    surface-cursor.c    \
    surface-shm.c       \
    shadow-screen.h     \
    shadow-screen.c     \
    $(NULL_FILE)

libnewgal_la_SOURCES = $(COMMON_SRCS)
libnewgal_la_LIBADD = $(DRIVERS)
libnewgal_la_DEPENDENCIES = $(DRIVERS)
