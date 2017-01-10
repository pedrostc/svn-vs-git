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

<<<<EXAMPLE - PHOENIX REPO>>>>
1.04 GB VS 425 MB

## Repository structure

On subversion you have a tree model with just on branch where the revisions, or commits, are stored on after the other.

GIT uses a Graph structure where each commit is a node that knows every of its parents. The commit is the central piece on the git repository.

## Branches

On the SVN side branches are just another directory on the repository with its own history information. You can merge revisions between branches but they are still treated as separated entities. Because of the centrelized nature of SVN all branches are remote and public. The administrator can restrict the access to the branch to a certains group of developers, but still, the branch is located on the server.

On git a branch is basically a named pointer for a specific commit on the tree, because of that branches are lightweight. Branches can be only local or can be published to a remote repository for collaboration with other developers. As the branch is create first locally, the user does not need to have access to the remote repository to complete this operation.
Every new copy of the repositroy, cloned from a remote repository, is by default a new local branch of the main repository, that means that every developer repository is a isolated entity and the work on that local repository does not intefeer with other developers work until it is pushed to the shared repository and unless the local copy is being used as a remote repository by another developer.

## Tags

Tags and branches are very similar in both systems. For SVN a TAG is just another folder on the main repository, that shouldn't receive any update and remaing static, that can be achieved using access restrictions on the new tag.

On git a tag is a static pointer to a specific commit. Unlike the branch pointer, the tag pointer is static, wich means that it cannot be moved to another commit.

## Commits

Every commit on SVN creates a nes revision on the remote repository, that means that, to be able to commit some changes on the code the developer need to have access to the main repository.

On git the commit is happens locally, so the developer does not need to have access to the remote. The work can be commited locally and then, when the developer gains access to the remote repository, it can push all the commits at once.

## Main workflow advantages

Some of the main advantages for the development workflow that git can provide are:

* - 