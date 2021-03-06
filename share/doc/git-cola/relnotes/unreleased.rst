.. _unreleased:

Latest Release
==============

:ref:`v2.3 <v2.3>` is the latest stable release.

Unreleased Topics
=================

Usability, bells and whistles
-----------------------------

* The user interface is now HiDPI-capable.  git-cola now uses SVG
  icons, and its interface can be scaled by setting the `GIT_COLA_SCALE`
  environment variable.

* `git dag` now supports the standard editor, difftool, and history hotkeys.
  It is now possible to invoke these actions from file widget's context
  menu and through the standard hotkeys.

  https://github.com/git-cola/git-cola/pull/473

* The `Status` tool also learned about the history hotkey.
  Additionally, the `Alt-{j,k}` aliases are also supported in the `Status`
  tool for consistency with the other tools where the non-Alt hotkeys are not
  available.

  https://github.com/git-cola/git-cola/pull/488

* The `File Browser` tool now has better default column sizes,
  and remembers its window size and placement.

* The `File Browser` now supports the refresh hotkey, and has better
  behavior when refreshing.  The selection is now retained, and new and
  removed files are found when refreshing.

Fixes
-----

* When using *Git for Windows*, a `git` window would appear on
  when running *Windows 8*.  We now pass additional flags to
  `subprocess.Popen` to prevent a `git` window from appearing.

  https://github.com/git-cola/git-cola/issues/477

  https://github.com/git-cola/git-cola/pull/486

* Launching difftool with `.PY` in `$PATHEXT` on Windows was fixed.

  https://github.com/git-cola/git-cola/issues/492

* Miscellaneous fixes

  https://github.com/git-cola/git-cola/pull/485

Packaging
---------

* git-cola's documentation no longer uses an intersphinx link mapping
  to docs.python.org.  This fixes warnings when building rpms using koji,
  where network access is prevented.

  https://bugzilla.redhat.com/show_bug.cgi?id=1231812

Development version
===================

Clone the git-cola repo to get the latest development version:

``git clone git://github.com/git-cola/git-cola.git``
