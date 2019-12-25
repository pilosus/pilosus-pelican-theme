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


### Minutes to read

Template gets use of [word count Pelican
plugin](https://github.com/pilosus/pilosus_pelican_word_count).  If
pluging is installed, add ``DISPLAY_WORD_COUNT`` variable to your
settings and set it to ``True`` in order to show number of words and
reading time in minutes in articles information block.


### Search input

Use ``DISPLAY_SEARCH`` boolean variable in your settings
(e.g. ``pelicanconf.py``) to enable/disable text input for Google
search.  Text submitted to the field is searched in Google with
``site:{{ SITEURL }}`` argument.

### Images


#### Floating left and right

reStructuredText ``image`` directive's ``align`` option has CSS
classes for both ``left`` and ``right`` floating:

```
.. image:: picture.jpeg
   :alt: alternate text
   :align: left
```

#### Responsive images

You can also make an image responsive (scaling up and down as you
resize browser window) with ``:class: responsive`` option in ``image``
directive:

```
.. image:: {static}/images/htop-minikube.png
   :alt: htop tool
   :class: responsive
   :target: {static}/images/htop-minikube.png
```

#### Rounded images

Use classes ``.circle`` and ``.rounded`` to render images with
``border-radius``.


### Table of Contents

[contents directive](http://docutils.sourceforge.net/docs/ref/rst/directives.html#table-of-contents)
generates a ``div`` block of class ``contents``. It's also got a CSS
style in ``custom.css``. Use it in your ``*.rst`` files like so:

```
.. contents::
```

### Disqus Comments

In order to activate [Disqus comments](https://disqus.com/)
``DISQUS_SITENAME`` and ``SITEURL`` variables in ``pelicanconf.py`` or
``publishconf.py``.

Comments are hidden for the drafts and articles with ``:comments: False`` in metadata.
