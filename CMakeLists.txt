cmake_minimum_required(VERSION 2.6)
project(Baselibc)
enable_testing()

include_directories(
	include
	src/templates
	)

set(SOURCES_LIB
	src/asprintf.c
	src/atoi.c
	src/atol.c
	src/atoll.c
	src/bsearch.c
	src/bzero.c
	src/calloc.c
	src/fgets.c
	src/inline.c
	src/jrand48.c
	src/lrand48.c
	src/malloc.c
	src/memccpy.c
	src/memchr.c
	src/memcmp.c
	src/memcpy.c
	src/memfile.c
	src/memmem.c
	src/memmove.c
	src/memrchr.c
	src/memset.c
	src/memswap.c
	src/mrand48.c
	src/nrand48.c
	src/qsort.c
	src/realloc.c
	src/sprintf.c
	src/srand48.c
	src/sscanf.c
	src/strcasecmp.c
	src/strcat.c
	src/strchr.c
	src/strcmp.c
	src/strcpy.c
	src/strcspn.c
	src/strdup.c
	src/strlcat.c
	src/strlcpy.c
	src/strlen.c
	src/strncasecmp.c
	src/strncat.c
	src/strncmp.c
	src/strncpy.c
	src/strndup.c
	src/strnlen.c
	src/strntoimax.c
	src/strntoumax.c
	src/strpbrk.c
	src/strrchr.c
	src/strsep.c
	src/strspn.c
	src/strstr.c
	src/strtoimax.c
	src/strtok.c
	src/strtok_r.c
	src/strtol.c
	src/strtoll.c
	src/strtoul.c
	src/strtoull.c
	src/strtoumax.c
	src/tinyprintf.c
	src/vasprintf.c
	src/vprintf.c
	src/vsprintf.c
	src/vsscanf.c
	)

add_library(c ${SOURCES_LIB})

set(SOURCES_TEST
	tests/printf_tests.c
	tests/tests_glue.c
	)
add_executable(tests ${SOURCES_TEST})
add_test(tests tests)
