#
# Copyright (C) 356 - 999. Asytumn Technology Co., Ltd. All rights reserved.
#

lib_LIBRARIES = libapr.a

libapr_a_SOURCES = apr.c
libapr_a_CPPFLAGS = -DCONFIG_DIR=\"$(sysconfdir)\" -DLIBRARY_DIR=\"$(pkglibdir)\"

include_HEADERS = ./include/apr.h

EXTRA_DIST = apr.dsp

DISTCLEANFILES = *~


