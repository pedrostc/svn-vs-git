Brainstorm
==========

- Licensing
    + Both are opensource

- Clients
    + SVN - Has the command line interface and some GUI clients like **Tortoise SVN** and **Visual SVN**.
    + GIT - Also has the command line interface and lots of GUI clients like **Git Extensions**, **Source Tree**, **GitHub**, **Git Kraken** and **Tortoise Git**.

- Type
    + SVN - CVCS (Centralized Version Control System) - There is just one central repository where all operations are performed and from where every user gets the files. This allows a top-down access control and change locking features.
    + GIT - DCVCS (Decentralized Version Control System) - Every user get a full copy of the repository on it's machine and, as a consequence, almost every operation is performed locally. There can be a central remote repository for collaboration to and from where the users will push and pull modifications. It also allows multiple remote repositories.

- Tree Model
    + SVN - Linear Tree (aka Stream) - SVN uses a linear tree as it's data structure which means that every single commit will be represented as a node on that tree (or line). Every merge from other branches results on a single new commit on the tree like any other modification.
    + GIT - DAG (Directed acyclic graph) [#]_ [#]_ - The GIT tree has a **Graph** where every commit has reference to, at least, one parent commit. This is specially helpful when you have branches and merges happening on your repository, this structure allows the user to find where each modification happened and in which branch it occurred. This struture maintains the whole commit history.

- Branching
    + SVN - As you have only the central repository every branch is automatically remote and public (every user with access to the repository will have access to the branch) [#]_ . On the other hand, one can checkout the branch on a different folder on it's file system independent of having the trunk of the repository checked-out. B
    + GIT - Branches

- Changes storage
    + SVN - Deltas
    + GIT - Files Snapshots


.. rubric:: Footnotes

.. [#] `SINK, Eric - Merge History, DAGs and Darcs <http://ericsink.com/entries/merge_history.html>`_
.. [#] `Wikipedia - Directed acyclic graph <https://en.wikipedia.org/wiki/Directed_acyclic_graph>`_
.. [#] CONFIRM THIS INFO
