# Copyright (c) 2014 Cesanta Software
# All rights reserved

CFLAGS = -W -Wall -I../.. -I. -g -O0 $(CFLAGS_EXTRA)

SOURCES = ws_ssl.c ../../mongoose.c net_skeleton.c ssl_wrapper.c
PROG = ws_ssl

all: $(PROG)

$(PROG): $(SOURCES)
	$(CC) -o $(PROG) $(SOURCES) \
		-DNS_ENABLE_SSL -DNOEMBED_NET_SKELETON \
		-DSSL_WRAPPER_USE_AS_LIBRARY -lssl $(CFLAGS)

clean:
	rm -rf $(PROG) *.exe *.dSYM *.obj *.exp .*o *.lib
