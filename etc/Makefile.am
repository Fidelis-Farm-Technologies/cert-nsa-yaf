##  Copyright 2005-2023 Carnegie Mellon University
##  See license information in LICENSE.txt.

##  Process this file with automake to produce Makefile.in
##  ------------------------------------------------------------------------
##  Makefile.am (startup)
##  autotools build system for NAF applications
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

# This is a sample yaf Lua-based configuration file that replaces most
# command line arguments.  Install it in $prefix/share/yaf/yaf.init
dist_pkgdata_DATA = yaf.init

# These are used to add yaf to the boot sequence.  Always install
# yaf.conf into $prefix/etc. We rely on rpmbuild to move init.d/yaf
# into place.
EXTRA_DIST = yaf.conf.in init.d/yaf.in

sysconf_DATA = yaf.conf

# Other config files that depend on how yaf is configured
dist_sysconf_DATA =

if PLUGINENABLE
dist_sysconf_DATA += dhcp_fingerprints.conf
endif

if DPIENABLE
dist_sysconf_DATA += yafDPIRules.conf
endif

if P0FENABLE
dist_sysconf_DATA += p0f.fp
endif
