Brainstorm
**********

Licensing
=========

- Both are opensource

Clients
=======

- SVN - Has the command line interface and some GUI clients like **Tortoise SVN** and **Visual SVN**.

- GIT - Also has the command line interface and lots of GUI clients like **Git Extensions**, **Source Tree**, **GitHub**, **Git Kraken** and **Tortoise Git**.

Type
====

- SVN - CVCS (Centralized Version Control System) - There is just one central repository where all operations are performed and from where every user gets the files. This allows a top-down access control and change locking features.

- GIT - DCVCS (Decentralized Version Control System) - Every user get a full copy of the repository on it's machine and, as a consequence, almost every operation is performed locally. There can be a central remote repository for collaboration to and from where the users will push and pull modifications. It also allows multiple remote repositories.

Tree Model
==========

- SVN - Linear Tree (aka Stream) - SVN uses a linear tree as it's data structure which means that every single commit will be represented as a node on that tree (or line). Every merge from other branches results on a single new commit on the tree like any other modification.

- GIT - DAG (Directed acyclic graph) [SINK1]_ [WIKI1]_ - The GIT tree has a **Graph** where every commit (graph node) has reference to, at least, one parent commit. This is specially helpful when you have branches and merges happening on your repository, this structure allows the user to find where each modification happened and in which branch it occurred. This struture maintains the whole commit history, even if some commits are not referenced by a branch or tag, they are still maintained on the RefLog and can be accessed.

Branching
=========

- SVN - Branches on SVN are treated as normal folders on the repository. As you have only the central repository every branch is automatically remote and public (every user with access to the repository will have access to the branch) [#]_ . On the other hand, one can checkout the branch on a different folder on it's file system independent of having the trunk of the repository checked-out. Another option is also start a branch on justa a subfolder of the repository. Branches on SVN are basically copies of the affected folders and this copy can be made locally and then commited to the central repo or remotly. On the remote copy it is made a *Cheap Copy* of the targeted files, this means that it is only a reference for the original files and not a actual file, this way the repository stay as lean as possible [#]_ .

    + "Subversion has no internal concept of a branch—it knows only how to make copies. When you copy a directory, the resultant directory is only a “branch” because you attach that meaning to it. You may think of the directory differently, or treat it differently, but to Subversion it's just an ordinary directory that happens to carry some extra historical information... Subversion's branches exist as normal filesystem directories in the repository." [COLLINS1]_

- GIT - Branches are pointers to specific commits on the repository. They are created locally and can be pushed/pulled to/from a remote repo or not.

Merge Process
=============

- SVN
- GIT

Changes storage
===============

- SVN - Deltas
- GIT - Files Snapshots

Commit structure
==================

- SVN
- GIT

.. rubric:: Footnotes

.. [#] CONFIRM THIS INFO
.. [#] Review text

.. rubric:: References

.. [SINK1] `Eric Sink - Merge History, DAGs and Darcs <http://ericsink.com/entries/merge_history.html>`_
.. [WIKI1] `Wikipedia - Directed acyclic graph <https://en.wikipedia.org/wiki/Directed_acyclic_graph>`_
.. [COLLINS1] `Ben Collins-Sussman, Brian W. Fitzpatrick & C. Michael Pilato - "Using Branches" in Version Control with Subversion <http://svnbook.red-bean.com/en/1.7/svn.branchmerge.using.html#svn.branchmerge.using.create>`_
