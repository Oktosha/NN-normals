# Project log & notes

Here you'll find almost all the things I've googled and all the problems I faced doing this project.
I hope such a log helps me next time :)

[What the hell is `.sudo_as_admin_successful`?](https://askubuntu.com/questions/813942/is-it-possible-to-stop-sudo-as-admin-successful-being-created)

[Oh, my.. don't you have pbcopy on Ubuntu?](https://garywoodfine.com/use-pbcopy-on-ubuntu/)

### ***

[Adding ssh-key](https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account) to GitHub:

1. Don't forget to [run `ssh-add`](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
2. Clonning the repo via ssh is the easiest way to configure repo to use ssh key


### ***

[Working with workspaces Ubuntu 18](https://help.ubuntu.com/stable/ubuntu-help/shell-windows.html.en)


### Conda envs
[Conda cheat sheet](https://conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)

```
$ conda create --name nn-norm
$ conda activate nn-norm
```

I had also to run `conda init zsh` ._.

When creating environment from file don't forget to specify the name, otherwise you face an uniformative error because you'll attempt to create a default environment.

```
conda env create --file environment.yml --name nn-norm
```

[Exporting environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#exporting-the-environment-file)

It's not that easy to share enviroment between macos and Ubuntu (I ended up maintaning 2 environments).

To make environment more portable, you can
[try to export it with `--no-builds`](https://github.com/conda/conda/issues/6073)

But I still faced problems with macos specific packages. Couldn't find the `--no-default-packages` option reccomended
[here](https://github.com/ContinuumIO/anaconda-issues/issues/10183)

```
Solving environment: failed

ResolvePackageNotFound: 
  - python.app=2
  - libcxxabi=4.0.1
  - libcxx=4.0.1

```

### ***

You need to set the `EDITOR` env variable to make vim the editor for git.

[tabs in kitty](https://sw.kovidgoyal.net/kitty/#id8)

[undo in git](https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git/)
