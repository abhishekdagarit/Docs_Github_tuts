Github pages, how to create them
===============================================

Creating Pages with the automatic generator
--------------------------------------------------------------

[Github source](https://help.github.com/articles/creating-pages-with-the-automatic-generator)

User and Org Pages
------------------------

To generate User and Organization pages, you'll need to create a repository named `username.github.io` or `orgname.github.io` first. The username or organization name must be your own or Pages will not build. The automatic page generator is accessible via the repository's admin page after you've created the repository.

The Automatic Page Generator
------------------------------------------

* Go to the repository's settings page
* Click the Automatic Page Generator button
* Author your content in the Markdown editor
* Click the Continue To Layouts button
* Preview your content in our themes
* When you find a theme that you like, click Publish

After your page is generated, you can get a local copy. If you generated a project page, fetch and check out the new branch:

```ruby
    $ cd repository
    $ git fetch origin
    remote: Counting objects: 92, done.
    remote: Compressing objects: 100% (63/63), done.
    remote: Total 68 (delta 41), reused 0 (delta 0)
    Unpacking objects: 100% (68/68), done.
    From https://github.com/user/repo.git
    * [new branch]      gh-pages     -> origin/gh-pages


    $ git checkout gh-pages
    Branch gh-pages set up to track remote branch gh-pages from origin.
    Switched to a new branch 'gh-pages'
```

If you generated a user page, the page code lives on the `master` branch instead of the `gh-pages` branch, so just check out `master` and then pull!

```ruby
    $ cd repository
    $ git checkout master
    Switched to branch 'master'
    $ git pull origin master
    remote: Counting objects: 92, done.
    remote: Compressing objects: 100% (63/63), done.
    remote: Total 68 (delta 41), reused 0 (delta 0)
    Receiving objects: 100% (424/424), 329.32 KiB | 178 KiB/s, done.
    Resolving deltas: 100% (68/68), done.
    From https://github.com/user/repo.git
    * branch      master     -> FETCH_HEAD
    Updating abc1234..def5678
    Fast-forward
    index.html                                     |  265 ++++
    ...
    98 files changed, 18123 insertions(+), 1 deletion(-)
    create mode 100644 index.html
    ...
```