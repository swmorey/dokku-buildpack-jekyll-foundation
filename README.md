# dokku-buildpack-jekyll

This is a dokku buildpack for [Jekyll Foundation](https://github.com/core77/jekyll-foundation) sites.  It is based on the official dokku nginx buildpack.

## Configuration

We are using this to deploy [planninglabs.nyc](https://github.com/nycplanning/labs-planninglabs.nyc), a Jekyll Foundation Site.  Since Jekyll Foundation requires yarn and gulp, we are combining this custom buildpack with the official nodejs buildpack.  Both are listed in `.buildpacks`.  

## History

This custom buildpack was originally for a simpler jekyll site, but we had to modify it to work with the more complex build of Jekyll Foundation.

After a compatibility issue with [this dokku jekyll buildpack](https://github.com/inket/dokku-buildpack-jekyll3-nginx) when deploying on Ubuntu 16.04.2, we needed a buildpack that would install a newer version of nginx.  This is based on the [official dokku nginx buildpack](https://github.com/dokku/buildpack-nginx), with the jekyll parts borrowed from [dokku-buildpack-jekyll3-nginx](https://github.com/inket/dokku-buildpack-jekyll3-nginx).

