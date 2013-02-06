# ghq - Tiny GitHub repositories manager

## USAGE

### Clone a repository

	% ghq [-clone] <repository url>

Clones target repository under `~/extrepo/@author/project` (configurable by `git config ghq.root`).

For example, `ghq -clone https://github.com/motemen/ghq`

 * clones repository into `~/extrepo/@motemen/ghq`
 * and creates a symlink `~/extrepo/ghq` linking to `@motemen/ghq`

### Chdir to a local repository

	% ghq [-cd] <repository name>

Changes pwd to the cloned repository.

### Execute a Git command on a local repository

	% ghq [-git] <repository name> <git subcommand> <arg> ...

## INSTALLATION

	% git clone git://github.com/motemen/ghq.git path_to_ghq_dir

Add in your .zshrc:

```shell
fpath=(path_to_ghq_dir $fpath)
autoload -U ghq
autoload -U compinit; compinit
```
