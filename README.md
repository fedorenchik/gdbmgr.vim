Gdbmgr: Gnu Debugger Manager for Vim
=====================================

DEPRECATION WARNING
-------------------

Since version 8.1 vim includes terminal debugger plugin which can be used
instead of this one and is preferred.

DISCLAIMER
----------

This plugin is by Dr Chip: http://www.drchip.org/astronaut/vim/index.html

All credits go to him.

### Why Distrubute on Github?

Distribute here for convenience (and to get rid of troubles to dealing with
archives).

DESCRIPTION
-----------

#### Updated Jun 01, 2017 (v2f)

[Manual]

[Manual]: http://www.drchip.org/astronaut/vim/doc/gdbmgr.txt.html

### Requirements: linux and a "huge" vim

Gdbmgr has two main components: a plugin portion, which provides an interface
for the user, and the second component, written in C, which provides
communications between vim and gdb. Gdbmgr works with core dumps, utilizes
hovering-cursor balloons to reveal variables' values, and provides a runtime
interface to your program via gdb and vim. It doesn't touch vim's source code
(no patches!) or need external interpreters, unlike several other ways to get
vim and gdb to work together.

 * GdbMgr provides an interface between vim and gdb: no patches!
 * No external interpreters are used (ie. no perl, no python, no ruby, ...)
 * Uses gcc to compile the component written in "C" GdbMgr requires a "huge" vim
 (configure --with-features=huge) with one or more of the following choices:
    - configure: --enable-perlinterp
    - configure: --enable-pythoninterp
    - have in Makefile: EXTRA_LIBS=-lutil
 * Integrated multi-window displays available include: Assembly, Breakpoints,
 Expressions, Function Stack, Messages, Source, Threads, and Watchpoints; it
 also supports in an integrated fashion "foreign apps": [Netrw], [CtagExpl], [HdrTag],
 and [bufexplorer]
 (thanks go to Jeff Lanzarotta for the last!).

 [Netrw]: http://www.drchip.org/astronaut/vim/index.html#NETRW
 [CtagExpl]: http://www.drchip.org/astronaut/vim/index.html#CTAGEXPL
 [HdrTag]: http://www.drchip.org/astronaut/vim/index.html#HDRTAGEXPLORER
 [bufexplorer]: http://www.vim.org/scripts/script.php?script_id=42

 * Customizable display (one may pick any subset of the integrated windows
   		 available and specify how they're to be displayed and/or
   		 stacked).
 * [Snapshot 1] This snapshot shows GdbMgr with a breakpoint and a temporary
 breakpoint in prog7's Func2() function.

 [Snapshot 1]: http://www.drchip.org/images/gdbmgr1.jpg

 * [Snapshot 2] This snapshot shows GdbMgr with the Command window having had

 [Snapshot 2]: http://www.drchip.org/images/gdbmgr2.jpg

 a dialog with the user (ie. "Enter something:", user entered "OK<cr>", etc.
 		 The program has run to completion.
 * Its distributed as a gzipped tarball instead of the vimball format usually
 used here as it contains some binaries (the two xpm files for the breakpoint
 	 signs)
 * Currently tested only under Linux; it definitely does need a Unix-like
 environment. I need a mac person to tell me how to get a shared library working
 on the Mac. I've included a first cut at it with Makefile.mac (under
 	 .vim/gdbmgr/src)
 * Integration with vim and gdb is provided by the plugin itself via vim's
 libcall() function and a small shared library written in C (code provided)
 * At the current time, gdbmgr has moved from alpha to beta (ie. majoring in bug
   	 removal, minoring in new features; its been working well lately).
 Please let me know if you experience problems (my email address is at the top
 	 of gdbmgr.vim).
