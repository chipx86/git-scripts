=============================
ChipX86's Git Utility Scripts
=============================

This is a repository of utility scripts for use with Git.  At the moment, it's
quite small (just one script).


Scripts
=======

git-hatchet
-----------

Splits apart a commit by file paths into new branches. git-hatchet is useful
when you've worked on a large change touching multiple components and want
to split it up for easy review or more fine-grained commits.

git-hatchet takes a branch and one or more paths (which may have wildcards).
It will operate on HEAD, taking every modified file in the paths and move them
to branch. HEAD will be updated to remove those files. If you pass
``--extract-only``, the files will remain in HEAD.

For example::

    $ git hatchet win32-changes src/win32/* docs/windows.txt
