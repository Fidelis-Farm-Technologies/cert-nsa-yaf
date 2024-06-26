##  Copyright 2006-2023 Carnegie Mellon University
##  See license information in LICENSE.txt.

##  Process this file with automake to produce Makefile.in
##  ------------------------------------------------------------------------
##  Makefile.am (source)
##  autotools build system for Airframe
##  ------------------------------------------------------------------------
##  Authors: Brian Trammell
##  ------------------------------------------------------------------------
##  @DISTRIBUTION_STATEMENT_BEGIN@
##  YAF 3.0.0
##
##  Copyright 2023 Carnegie Mellon University.
##
##  NO WARRANTY. THIS CARNEGIE MELLON UNIVERSITY AND SOFTWARE ENGINEERING
##  INSTITUTE MATERIAL IS FURNISHED ON AN "AS-IS" BASIS. CARNEGIE MELLON
##  UNIVERSITY MAKES NO WARRANTIES OF ANY KIND, EITHER EXPRESSED OR IMPLIED,
##  AS TO ANY MATTER INCLUDING, BUT NOT LIMITED TO, WARRANTY OF FITNESS FOR
##  PURPOSE OR MERCHANTABILITY, EXCLUSIVITY, OR RESULTS OBTAINED FROM USE OF
##  THE MATERIAL. CARNEGIE MELLON UNIVERSITY DOES NOT MAKE ANY WARRANTY OF
##  ANY KIND WITH RESPECT TO FREEDOM FROM PATENT, TRADEMARK, OR COPYRIGHT
##  INFRINGEMENT.
##
##  Licensed under a GNU GPL 2.0-style license, please see LICENSE.txt or
##  contact permission@sei.cmu.edu for full terms.
##
##  [DISTRIBUTION STATEMENT A] This material has been approved for public
##  release and unlimited distribution.  Please see Copyright notice for
##  non-US Government use and distribution.
##
##  GOVERNMENT PURPOSE RIGHTS – Software and Software Documentation
##  Contract No.: FA8702-15-D-0002
##  Contractor Name: Carnegie Mellon University
##  Contractor Address: 4500 Fifth Avenue, Pittsburgh, PA 15213
##
##  The Government's rights to use, modify, reproduce, release, perform,
##  display, or disclose this software are restricted by paragraph (b)(2) of
##  the Rights in Noncommercial Computer Software and Noncommercial Computer
##  Software Documentation clause contained in the above identified
##  contract. No restrictions apply after the expiration date shown
##  above. Any reproduction of the software or portions thereof marked with
##  this legend must also reproduce the markings.
##
##  This Software includes and/or makes use of Third-Party Software each
##  subject to its own license.
##
##  DM23-2317
##  @DISTRIBUTION_STATEMENT_END@
##  ------------------------------------------------------------------------

AM_CFLAGS = $(WARN_CFLAGS) $(DEBUG_CFLAGS)
AM_CPPFLAGS = $(YAF_CPPFLAGS) $(GLIB_CFLAGS)
AM_LDFLAGS = $(GLIB_LIBS)
LDADD = $(GLIB_LDADD) libairframe.la

lib_LTLIBRARIES = libairframe.la
bin_PROGRAMS = airdaemon filedaemon

libairframe_la_SOURCES = airutil.c daeconfig.c logconfig.c privconfig.c \
        mio.c mio_stdio.c mio_source_file.c mio_sink_file.c \
        mio_common_net.c mio_source_udp.c mio_sink_udp.c \
        mio_source_tcp.c mio_sink_tcp.c \
        mio_source_pcap.c mio_sink_multi.c mio_config.c \
        airopt.c airlock.c
libairframe_la_LIBADD = $(GLIB_LDADD)
libairframe_la_LDFLAGS = $(GLIB_LIBS) -version-info $(LIBCOMPAT) \
    -release ${VERSION}

airdaemon_SOURCES = airdaemon.c

filedaemon_SOURCES = filedaemon.c

noinst_HEADERS = mio_internal.h mio_common_net.h
