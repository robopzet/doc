# git
Full command [reference](https://git-scm.com/docs).


## Commands
### [git add](https://git-scm.com/docs/git-add) options \<pathspec>
Stage files mathing `<pathspec>` for commit. `<pathspec>` __*__ adds all in
repo.

* `-n` dry-run, show files that would be added/ignored.
* `-p` Interactively stage parts (hunks) of files.


### [git branch](https://git-scm.com/docs/git-branch)
Manage branches.

Without options it lists the branches.

* `-d <name>` delete branch `<name>`.
* `<name>` create a branch `<name>`.


### [git checkout](https://git-scm.com/docs/git-checkout)
Switch branches or restore working tree files.

* `<branch>` switch working tree to `<branch>`.
* `-b <branch>` create a branch named `<branch>` and switch to it.


### [git clone](https://git-scm.com/docs/git-clone) \<URL>
Clone a repository into a new directory.


### [git commit](https://git-scm.com/docs/git-commit)
Commit changes from the staging area. Without options the default editor opens
to enter the commit message.

* `-m "<msg>"` include the commit message `<msg>` on the command line. The
  editor will not be used.
* `--amend` change the latest commit to include extra file changes or change
  the commit message. **Do not use this when the commit is already pushed to a
  shared repository**.


### [git config](https://git-scm.com/docs/git-config) --global core.editor \<cmd>
Set editor, for things like commit messages, to `<cmd>`, for example

    "'C:\Program Files (x86)\Notepad++\notepad++.exe' -multiInst -notabbar -nosession -noPlugin"

Note the single plus double quotes are needed on Windows or git cannot open the
program. The additionl options are specific for Notepad++ to create a basic new
instance without other tabs. Found
[here](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/How-to-set-Notepad-as-the-default-Git-editor-for-commits-instead-of-Vim).


### [git diff](https://git-scm.com/docs/git-diff)
Shows differences between all changed files in working tree and HEAD.

* `<file>` shows only the differences of \<file>.


### [git init](https://git-scm.com/docs/git-init)
Creates an initial Git repository from the current directory. It creates the
**.git** directory. The common next step is to create a **.gitignore** file.


### [git log](https://git-scm.com/docs/git-log)
Show commit logs

* `--name-only`: include names of changed files in output.
* `--oneline`: shows commit hash and first line of the message (alias for
  `git log --pretty=oneline --abbrev-commit`).
* `-- <path>`: show log of `<path>`.
* `<tag-1>..<tag-2>`: log commits between `<tag-1>` and `<tag-2>`.


### [git push](https://git-scm.com/docs/git-push)
Send changes from the local repo to the remote repo.

Tags are not included by default. To push a single tag use
`git push origin <tagname>`. To push all tags that are not present in the
remote repo use `git push origin --tags`.

* `-u origin <branch>` add branch `<branch>` that exists locally but not
  remote, to the remote repo, like GitHub.


### [git remote](https://git-scm.com/docs/git-remote) \<command>
From git manual: _Manage the set of repositories ("remotes") whose branches you
track._


* `prune <name> [--dry-run]` delete references to local branches that no longer
  exist on the remote repo `<name>` Normally, the `<name>` **origin** refers to
  the repo on GitHub. `--dry-run` lists what would be deleted, without doing
  it. Branches itself are not deleted.


### [git restore](https://git-scm.com/docs/git-restore) \<file>
Restore the version of `<file>`. If `<file>` is changed but not staged,
restores to the version before the changes.


### [git show](https://git-scm.com/docs/git-show)
Show commits including file changes.


### [git status](https://git-scm.com/docs/git-status)
Show untracked files and changed files that are not staged.


### [git tag](https://git-scm.com/docs/git-tag)
Show and manage tags. See `git push` for information about pushing tags to a
remote repo.

* `-a <version>` create an annoted tag for `<version>`.
* `-m` the message for the tag. If omitted the configured editor opens to
  enter the message.
