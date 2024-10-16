# YMMOR Homepage

The YMMOR homepage is a static homepage created with the tool 
[hugo](https://gohugo.io). It is hostet via github pages and can be reached 
[here](https://ymmor-conferences.github.io/)


## Building the site
If content is added or changed the site needs to be rebuilt. If you push the changes, this 
automatically done via a github workflow. In order to build a version
locally first, `hugo` needs to be installed (currently version 0.132.2. is used)

The site can then be built with the command executed from the base directory of the
repository

    hugo -d docs

the target directory needs to be set to `docs`, otherwise github pages won't
display the page properly. To include drafts in the built the option `-D` also
needs to be passed

    hugo -D -d docs

If you are using an older version of `hugo` you might need to explicitly specify the
config file with `--config hugo.toml`.

### Installing the theme
The page uses a modified version of the theme
[beautifulhugo](https://github.com/halogenica/beautifulhugo)
If the repository is freshly cloned the theme for the page needs to be pulled.
The theme is included as a git submodule. To get the theme one just needs to run

    git submodule init
    git submodule update

### Local Preview
The page can be locally previewed when working on the page just run

    hugo -D server

in an additional terminal. The site can than be reached at
[localhost:1313/](localhost:1313/). The page is automatically
rebuild if any file is changed.

## Content

The content of the page(s) can be edited within the `content` folder. Everything
here is written in `markdown` Syntax. To add, for example a new conference, the
(including its header) can be added with:

    hugo new conferences/your_new_file.md

To change the menus etc. the file `hugo.toml` needs to be adapted.

Examples with pictures etc can be found in `themes/beautifulhugo/exampleSite/content/post/`
