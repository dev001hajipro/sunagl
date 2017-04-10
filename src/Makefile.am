# why bin_ ? cause /usr/local/bin
bin_PROGRAMS = sunagl
sunagl_CFLAGS = -Wall -Wextra -pedantic -std=c11 $(GLU_CFLAGS)
sunagl_SOURCES = \
    sunagl.c \
    greeting.h \
    greeting.c
sunagl_LDADD = -lm $(GLU_LIBS)
