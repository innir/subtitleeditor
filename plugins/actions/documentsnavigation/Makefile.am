pluginlibdir = $(PACKAGE_PLUGIN_LIB_DIR)/actions
plugindescriptiondir = $(PACKAGE_PLUGIN_DESCRIPTION_DIR)/actions
actionsharedir = $(PACKAGE_PLUGIN_SHARE_DIR)/actions

AM_CPPFLAGS = \
	 -I$(top_srcdir) \
	 -I$(top_srcdir)/src \
	 $(SUBTITLEEDITOR_CFLAGS)

pluginlib_LTLIBRARIES = \
	libdocumentsnavigation.la

libdocumentsnavigation_la_SOURCES = \
	documentsnavigation.cc

libdocumentsnavigation_la_LDFLAGS = $(PLUGIN_LIBTOOL_FLAGS)
libdocumentsnavigation_la_LIBADD = \
	$(SUBTITLEEDITOR_LIBS) \
	-L$(top_srcdir)/src -lsubtitleeditor

plugindescription_in_files = documentsnavigation.se-plugin.in
plugindescription_DATA = $(plugindescription_in_files:.se-plugin.in=.se-plugin)

@INTLTOOL_SE_PLUGIN_RULE@

EXTRA_DIST = $(plugindescription_in_files)

CLEANFILES = $(plugindescription_DATA) Makefile.am~ *.cc~ *.h~ *.in~
