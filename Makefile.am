AM_CPPFLAGS = -I$(srcdir)/include
AM_CFLAGS = -Wall
bin_PROGRAMS = tio
tio_SOURCES = tty.c \
              upgrades.c \
              options.c \
              time.c \
              main.c \
              log.c \
              error.c \
              include/tio/tty.h \
              include/tio/upgrades.h \
              include/tio/options.h \
              include/tio/time.h \
              include/tio/print.h \
              include/tio/log.h \
              include/tio/error.h

if ADD_SETSPEED2
tio_SOURCES += setspeed2.c
endif

if ENABLE_BASH_COMPLETION
bashcompletiondir=@BASH_COMPLETION_DIR@
bashcompletion_DATA=bash-completion/tio
endif
