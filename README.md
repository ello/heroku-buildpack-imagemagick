heroku-buildpack-imagemagick
=================================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for vendoring the ImageMagick binaries into your project.

## Note on Heroku config

Optionally, set the ImageMagick version in a Heroku config like this:

```
heroku config:set IMAGE_MAGICK_VERSION=7.0.5-0
```

Make sure the version you're referencing exists on as a `.tar.xz` file amon the [ImageMagic releases](http://www.imagemagick.org/download/releases/).

(Buildpack developer note: the config setting does not show up in the compile script as an environment variable, and has to be read from a file in `$3`, as explained in the [Heroku buildpack docs](https://devcenter.heroku.com/articles/buildpack-api#bin-compile-summary).)
