
TESTS_ENVIRONMENT = $(SHELL) $(top_builddir)/TESTS_ENVIRONMENT

AM_CPPFLAGS = \
	-I$(top_srcdir)/src \
	$(SQLITE3_CFLAGS)

# AM_CFLAGS = -fprofile-arcs -ftest-coverage
# AM_CXXFLAGS = -fprofile-arcs -ftest-coverage

check_PROGRAMS = \
	drive_line_buffer \
	drive_grep_proc \
	drive_listview \
	drive_logfile \
	drive_vt52_curses \
	drive_readline_curses \
	slicer \
	scripty \
	test_auto_fd \
	test_auto_mem \
	test_bookmarks \
	test_grep_proc2 \
	test_line_buffer2 \
	test_top_status

AM_LDFLAGS = \
	$(SQLITE3_LDFLAGS)

LDADD = -lz

test_auto_fd_SOURCES = test_auto_fd.cc

test_auto_mem_SOURCES = test_auto_mem.cc

test_bookmarks_SOURCES = test_bookmarks.cc ../src/bookmarks.cc

test_grep_proc2_SOURCES = \
	../src/line_buffer.cc \
	../src/grep_proc.cc \
	test_grep_proc2.cc
test_grep_proc2_LDADD = $(PCRE_LIBS) -lz

test_line_buffer2_SOURCES = \
	../src/line_buffer.cc \
	test_line_buffer2.cc

test_top_status_SOURCES = \
	../src/bookmarks.cc \
	../src/logfile.cc \
	../src/line_buffer.cc \
	../src/log_format.cc \
	../src/logfile_sub_source.cc \
	../src/listview_curses.cc \
	../src/textview_curses.cc \
	../src/view_curses.cc \
	test_top_status.cc
test_top_status_LDADD = $(CURSES_LIB) -lz

drive_line_buffer_SOURCES = \
	../src/line_buffer.cc \
	drive_line_buffer.cc
drive_line_buffer_LDADD = $(CURSES_LIB) -lz

drive_grep_proc_SOURCES = \
	../src/line_buffer.cc \
	../src/grep_proc.cc \
	drive_grep_proc.cc
drive_grep_proc_LDADD = $(PCRE_LIBS) -lz

drive_listview_SOURCES = \
	../src/listview_curses.cc \
	../src/view_curses.cc \
	drive_listview.cc
drive_listview_LDADD = $(CURSES_LIB) -lz

drive_logfile_SOURCES = \
	../src/logfile.cc \
	../src/log_format.cc \
	../src/line_buffer.cc \
	drive_logfile.cc

drive_vt52_curses_SOURCES = \
	../src/vt52_curses.cc \
	drive_vt52_curses.cc
drive_vt52_curses_LDADD = $(CURSES_LIB)

drive_readline_curses_SOURCES = \
	../src/vt52_curses.cc \
	../src/readline_curses.cc \
	drive_readline_curses.cc
drive_readline_curses_LDADD = $(CURSES_LIB) $(READLINE_LIBS)

slicer_SOURCES = \
	../src/line_buffer.cc \
	slicer.cc

scripty_SOURCES = scripty.cc

dist_noinst_SCRIPTS = \
	test_grep_proc.sh \
	test_line_buffer.sh \
	test_listview.sh \
	test_logfile.sh \
	test_vt52_curses.sh

dist_noinst_DATA = \
	listview_output.0 \
	listview_output.1 \
	listview_output.2 \
	listview_output.3 \
	listview_output.4 \
	listview_output.5 \
	listview_output.6 \
	logfile_access_log.0 \
	logfile_empty.0 \
	logfile_syslog.0 \
	logfile_syslog.1 \
	logfile_tcsh_history.0 \
	logfile_with_a_really_long_name_to_test_a_bug_with_long_names.0 \
	vt52_curses_input.0 \
	vt52_curses_input.1 \
	vt52_curses_output.0 \
	vt52_curses_output.1

TESTS = test_bookmarks \
	test_auto_fd \
	test_auto_mem \
	test_line_buffer.sh \
	test_line_buffer2 \
	test_grep_proc.sh \
	test_grep_proc2 \
	test_listview.sh \
	test_logfile.sh \
	test_vt52_curses.sh \
	test_top_status