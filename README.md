# Pilosus Pelican Theme

`Pilosus Pelican Theme` is a minimalistic theme for
[Pelican](https://docs.getpelican.com/en/stable/) based on Pelican's 4.0.1 default theme, 
a lightweight responsive [Skeleton CSS Boilerplate](http://getskeleton.com/) and 
[Pygments](http://pygments.org/) for code syntax highlighting.


## Installation

1. Get the theme files:

```
$ git clone https://github.com/pilosus/pilosus-pelican-theme.git
```
or go get an archive at:

```
$ browser https://github.com/pilosus/pilosus-pelican-theme/releases
```
2. (Optional) You can add the theme repo as a submodule in your blog
   repository:

```
$ cd your-blog-repo
$ git submodule add https://github.com/pilosus/pilosus-pelican-theme.git
```

It allows you to use `git submodule update` to get the latest version
of the theme.


3. Generate your static website with a path to the theme:

```
$ pelican content -s pelicanconf.py -t /your/path/to/pilosus-pelican-theme
```
You can also define `THEME` variable in your settings to point to the
location of your preferred theme.


## Usage

Based on Skeleton CSS, the theme supports all its typography. A few style classes were added to
[customs.css](https://github.com/pilosus/pilosus-pelican-theme/blob/master/static/css/custom.css)
to play nicely with some [reStructuredText directives](http://docutils.sourceforge.net/docs/ref/rst/directives.html)
and their options.

### Images

reStructuredText ``image`` directive's ``align`` option has CSS
classes for both ``left`` and ``right`` floating:

```
.. image:: picture.jpeg
   :alt: alternate text
   :align: left
```
