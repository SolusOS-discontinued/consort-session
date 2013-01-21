bin_PROGRAMS = consort-session-quit
libexec_PROGRAMS = consort-session-check-accelerated consort-session-check-accelerated-helper

AM_CPPFLAGS =

AM_CFLAGS = $(WARN_CFLAGS)

consort_session_quit_SOURCES =			\
	consort-session-quit.c

consort_session_quit_CPPFLAGS =			\
	$(AM_CPPFLAGS)				\
	$(CONSORT_SESSION_CFLAGS)			\
	$(DBUS_GLIB_CFLAGS)			\
	$(GCONF_FLAGS)				\
	-DLOCALE_DIR=\""$(datadir)/locale"\"	\
	$(DISABLE_DEPRECATED_CFLAGS)

consort_session_quit_LDADD =			\
	$(SM_LIBS)				\
	$(ICE_LIBS)				\
	$(CONSORT_SESSION_LIBS)			\
	$(DBUS_GLIB_LIBS)			\
	$(GCONF_LIBS)

consort_session_check_accelerated_helper_SOURCES = 		\
	consort-session-check-accelerated-helper.c

consort_session_check_accelerated_helper_CPPFLAGS =	\
	-DPKGDATADIR=\""$(pkgdatadir)"\"		\
	$(GL_TEST_CFLAGS)

consort_session_check_accelerated_helper_LDADD = 		\
	$(GL_TEST_LIBS)				\
	$(X_LIBS)

consort_session_check_accelerated_SOURCES =       \
	consort-session-check-accelerated.c

consort_session_check_accelerated_CPPFLAGS =      \
	-DLIBEXECDIR=\""$(libexecdir)"\"	\
	$(AM_CPPFLAGS)			        \
	$(GTK3_CFLAGS)

consort_session_check_accelerated_LDADD =         \
	$(GTK3_LIBS)				\
	$(X_LIBS)

-include $(top_srcdir)/git.mk
