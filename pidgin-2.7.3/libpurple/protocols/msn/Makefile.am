EXTRA_DIST = \
	directconn.c \
	directconn.h \
	Makefile.mingw

pkgdir = $(libdir)/purple-$(PURPLE_MAJOR_VERSION)

MSNSOURCES = \
	cmdproc.c \
	cmdproc.h \
	command.c \
	command.h \
	contact.c\
	contact.h\
	dialog.c \
	dialog.h \
	directconn.c \
	directconn.h \
	error.c \
	error.h \
	group.c \
	group.h \
	history.c \
	history.h \
	httpconn.c \
	httpconn.h \
	msg.c \
	msg.h \
	msn.c \
	msn.h \
	nexus.c \
	nexus.h \
	notification.c \
	notification.h \
	object.c \
	object.h \
	oim.c\
	oim.h\
	page.c \
	page.h \
	servconn.c \
	servconn.h \
	session.c \
	session.h \
	slp.c \
	slp.h \
	slpcall.c \
	slpcall.h \
	slplink.c \
	slplink.h \
	slpmsg.c \
	slpmsg.h \
	soap.c \
	soap.h \
	state.c \
	state.h \
	switchboard.c \
	switchboard.h \
	sync.c \
	sync.h \
	table.c \
	table.h \
	transaction.c \
	transaction.h \
	user.c \
	user.h \
	userlist.c \
	userlist.h \
	msnutils.c \
	msnutils.h

AM_CFLAGS = $(st)

libmsn_la_LDFLAGS = -module -avoid-version

if STATIC_MSN

st = -DPURPLE_STATIC_PRPL
noinst_LTLIBRARIES = libmsn.la
libmsn_la_SOURCES  = $(MSNSOURCES)
libmsn_la_CFLAGS   = $(AM_CFLAGS)

else

st =
pkg_LTLIBRARIES   = libmsn.la
libmsn_la_SOURCES = $(MSNSOURCES)
libmsn_la_LIBADD  = $(GLIB_LIBS)

endif

AM_CPPFLAGS = \
	-I$(top_srcdir)/libpurple \
	-I$(top_builddir)/libpurple \
	$(GLIB_CFLAGS) \
	$(DEBUG_CFLAGS)
