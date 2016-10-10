# Magenta Blog

This blog is generated using [Jekyll](http://jekyllrb.com). Posts to the blog
are under the `_posts` directory.

## Previewing posts

### Installing Jekyll

To preview posts, you must first install Jekyll. Installing Jekyll locally
requires a newer version of Ruby than is currently available on Goobuntu.
[RVM](https://rvm.io) is the best way to install a newer version of Ruby without
affecting the rest of your system. You can then install Jekyll using gem.

Here is the complete set of installation commands:

```bash
$ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
$ \curl -sSL https://get.rvm.io | bash -s stable --ruby
$ source ~/.rvm/scripts/rvm
$ gem install jekyll
```

### Previewing in Jekyll

After editing files here, run `jekyll build` from within this directory. That
will generate a static version of the blog under the `_site` directory. If you
would like to see local preview of what the published blog will look like, run
`jekyll serve -H $HOSTNAME`.

## Submitting changes

Be sure to run `jekyll build` before sending out your CL so your change will
include updates to the generated static site. You may need to do `g4 reopen`
after building the site so that Piper knows about all the changed files.

## Deploying

To deploy a new version of the blog to appengine, use this script:
`/google/src/head/depot/google3/learning/brain/research/magenta/blog/update_blog.sh`

If called with no parameters, this script will stage changes
locally using the version of the blog in the current google3 workspace.
A local server will be started, serving the page from http://localhost:8888/.

If called with `--staging`, this script will deploy the version of the blog in
google3 HEAD to http://magenta-staging.tensorflow.org/.

If called with `--deploy`, this script will deploy the version of the blog in
google3 HEAD to http://magenta.tensorflow.org/.
Please verify that you have first deployed to staging first and checked that
http://magenta-staging.tensorflow.org looks correct.
