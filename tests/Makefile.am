######################### CS COMMON VARIABLE ############################

if DEBUG
DEBUG_CFLAGS = -g -ggdb
else
DEBUG_CFLAGS =
endif

######################### CS SQL QUERY TEST APPS ############################
bin_PROGRAMS = cs_sql_test

cs_sql_test_SOURCES = cs_sql_test.c

cs_sql_test_CPPFLAGS = $(MYSQL_CONFIG_CPPFLAGS)

cs_sql_test_CFLAGS = $(DEBUG_CFLAGS) -std=c99 -D_BSD_SOURCE -D_DEFAULT_SOURCE -I$(top_srcdir)/src/include \
					 -Wall $(MYSQL_CONFIG_CFLAGS)

cs_sql_test_LDADD = -lcssql -L./../src $(MYSQL_CONFIG_LIBS)
