# SVN x GIT

## Centralized VS Distributed

 - |Centralized|Distributed
:---:|:---:|:---:
Repository Location|Remote server|Local - There can be a central repository on a remote server but every collaborator who is working on it has a full copy of the repository locally.
Operations|Remote|Mostly local

## Space Consumption

Knowing that when one developer clone a GIT repository it actually gets a full copy of the intere repository, a concern may araise in terms os local disk space consumption. Well, while you may have more data stored in your disk all the GIT database is compressed and highly optimized wich means that the local repository will ocupy less space in disk than one may think.

When you checkout a sa folder from a subversion repository you end up with 2 uncompressed versions of the folder locally, your working copy and the snapshot of the last revision, the one you checkd out, of the folder. SVN does that to allow the developer to make diffs between the working copy and the last revision locally without needing to go to the server.

We can compare the two options to see wich has the biggest size, that can be done importing a existing SVN repository to a GIT repository using the GIT-SVN tool and then compare sizes on the folders.

<<<<EXAMPLE - PHOENIX REPO>>>
1.04 GB VS 425 MB