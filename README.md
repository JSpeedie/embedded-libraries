# embedded-libraries

A collection of libraries I wrote for various embedded peripherals.

The point of this repository is to provide a simple way to find and view
the libraries I have written. Click on the submodule links in the file list
of this repo to visit the library pages which have more information about
themselves.


## Cloning

Because this repository is just a collection of submodules which point to completed
libraries, we need to clone the repo using:

```bash
git clone --recursive git@github.com:JSpeedie/embedded-libraries.git embedded-librariesGit
```


## Maintenance

### Adding another library (as a submodule):

Adding a new library is simple:

```bash
cd embedded-librariesGit/
# To add the submodule and to have it track the main branch of its repo
git submodule add -b main [url to git repo]
```

<details><summary>Instructions on how to get an already-added submodule to track main (Click to Expand)</summary><p>

If you have already added the submodule but want it to track the `main` branch
of its repo rather than a specific commit, instead of running the previous
command, you can do the following:

```bash
git config -f .gitmodules submodule.[name of git repo].branch main
cd [name of git repo]
git branch -u origin/main main
```
</p></details>

With the submodule now added and tracking main, we can commit and push:

```bash
git commit -m [commit message]
git push
```

### Updating the libraries

Since the links in this repo to the library repos can get out of date,
here's the command sequence to update them:

```bash
git submodule update --remote --merge
git commit -am "Updated the libraries"
git push
```
