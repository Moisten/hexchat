localedir = $(datadir)/locale

bin_PROGRAMS = hexchat

AM_CPPFLAGS = $(GUI_CFLAGS) -DG_DISABLE_CAST_CHECKS -DLOCALEDIR=\"$(localedir)\"

hexchat_LDADD = ../common/libhexchatcommon.a $(GUI_LIBS)

EXTRA_DIST = \
	about.h ascii.h banlist.h chanlist.h chanview.h chanview-tabs.c \
	chanview-tree.c custom-list.h editlist.h fe-gtk.h fkeys.h gtkutil.h joind.h \
	maingui.h menu.h mmx_cmod.S mmx_cmod.h notifygui.h palette.h pixmaps.h \
	plugin-tray.h plugingui.c plugingui.h rawlog.h search.h sexy-iso-codes.h \
	sexy-spell-entry.h sexy-marshal.h textgui.h urlgrab.h userlistgui.h xtext.h

if USE_MMX
mmx_cmod_S = mmx_cmod.S
endif

if DO_PLUGIN
plugingui_c = plugingui.c
endif

if USE_LIBSEXY
sexy_spell = \
	sexy-iso-codes.c sexy-marshal.c sexy-spell-entry.c
endif

hexchat_SOURCES = about.c ascii.c banlist.c chanlist.c chanview.c custom-list.c \
	dccgui.c editlist.c fe-gtk.c fkeys.c gtkutil.c ignoregui.c joind.c menu.c \
	maingui.c $(mmx_cmod_S) notifygui.c palette.c pixmaps.c plugin-tray.c $(plugingui_c) \
	rawlog.c search.c servlistgui.c setup.c $(sexy_spell) textgui.c \
	urlgrab.c userlistgui.c xtext.c
