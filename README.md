# embedded-libraries
A collection of libraries I wrote for various embedded peripherals


## Cloning

Because this repository is just a collection of submodules which point to completed
libraries, we need to clone the repo using:

```bash
git clone --recursive git@github.com:JSpeedie/embedded-libraries.git embedded-librariesGit
```


## Maintenance

To add another library as a submodule:

```bash
cd embedded-librariesGit/
# To add the submodule and to have it track the main branch of its repo
git submodule add -b main [url to git repo]
```

If you have already added the submodule but want it to track the `main` branch
of its repo rather than a specific commit, instead of running the previous
command, you can do the following:

```bash
git config -f .gitmodules submodule.[name of git repo].branch main
cd [name of git repo]
git branch -u origin/main main
```

With the submodule now added and tracking main, we can commit and push:

```bash
git add .gitmodules
git add [name of git repo]
git commit -m [commit message]
git push
```
