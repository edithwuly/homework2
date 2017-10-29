# Git workflow
## SVN?
- an open-source, centralized version control system
- a single central repository as the communication hub for developers
- collaboration takeing place by passing changesets between the developers’ working copies and the central repository
## Git?
- a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel 
- an example of a DVCS (hence Distributed Version Control System)
- every developer having their own copy of the repository, complete with its own local history and branch structure

## Workflow?
>A workflow consists of an orchestrated and repeatable pattern of business activity enabled by the systematic organization of resources into processes that transform materials, provide services, or process information.

## Git Workflow?
>A Git Workflow is a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner. 

### Why Git?
#### feature branches
- cheap and easy to merge
- an isolated environment
- the master branch always contains production-quality code
- organizational benefits

#### distributed development
- SVN: each developer gets a working copy that points back to a single central repository
- Git: each developer gets their own local repository, complete with a full history of commits
- less dependence on a network connection
- easier to scale the team
- more reliable environment

#### pull request
- a way to ask another developer to merge one of your branches into their repository
- easier for project leads to keep track of changes
- lets developers initiate discussions around their work before integrating it with the rest of the codebase

#### stable community
- no  need to train new hires on the workflow
- easy to leverage 3rd-party libraries and encourage others to fork your own open source code

#### faster release cycle
- developers being encouraged to share smaller changes more frequently
- changes can get pushed down the deployment pipeline faster 

## Common Git Workflows for Software Teams

### Centralized Workflow
- transitioning from SVN
- a central repository as the single point-of-entry for all changes to the project
- the default development branch being called master and all changes being committed into this branch
- no requiring any other branches besides master

![](https://segmentfault.com/image?src=http://static.ixirong.com/pic/gitflow/git-workflow-svn-push-local.png&objectId=1190000002918123&token=cb6d4428bd989a9db24ea68b29588a67)

#### Advantages:
1. no need to change existing workflow 
2. not affected by upstream developments
3. access to Git’s robust branching and merging model

#### Suit:
teams migrating from SVN to Git and smaller size teams

### Feature Branch Workflow
- a logical extension of Centralized Workflow
- all feature development taking place in a dedicated branch 

![](https://sfault-image.b0.upaiyun.com/135/687/1356871362-56fe09a564c99_articlex)

#### Advantage:
1. isolated experiments
2. master branch always containing production-quality code
3. possible to leverage pull requests, easy to comment on each other’s work
4. composable


### Gitflow Workflow
- a strict branching model designed around the project release
- not new concepts or commands beyond what’s required for the Feature Branch Workflow
- assigning specific roles to different branches and defining how and when they should interact
-  using individual branches for preparing, maintaining, and recording releases

![](https://sfault-image.b0.upaiyun.com/221/358/2213586864-56fe8ad48caf1_articlex)

#### Advantages:
1. providing a robust framework for managing larger projects  
2. all the benefits of the Feature Branch Workflow

#### Suit:
projects that have a scheduled release cycle

### Forking Workflow
- every developer having a server-side repository
- complete feature branches being purposed for merge into the original project maintainer's repository

![](https://sfault-image.b0.upaiyun.com/348/941/3489415854-56feaa016d70d_articlex)

#### Advantages:
1. contributions can be integrated without the need for everybody to push to a single central repository
2. a flexible way for large, organic teams (including untrusted third-parties) to collaborate securely

#### Suit:
public open source projects
