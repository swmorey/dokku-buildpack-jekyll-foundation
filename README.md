# dokku-buildpack-jekyll

This is a dokku buildpack for jekyll 3 sites, powered by nginx.

## About

After a compatibility issue with [this dokku jekyll buildpack](https://github.com/inket/dokku-buildpack-jekyll3-nginx) when deploying on Ubuntu 16.04.2, we needed a buildpack that would install a newer version of nginx.  This is based on the [official dokku nginx buildpack](https://github.com/dokku/buildpack-nginx), with the jekyll parts borrowed from [dokku-buildpack-jekyll3-nginx](https://github.com/inket/dokku-buildpack-jekyll3-nginx).

### Dokku

To trigger detection of this buildpack you need to add a dotfile:

Add an *empty* file called `.static` to your root directory of your web project (regardless if you use a custom value for NGINX_ROOT)


## Configuration

You can override the nginx root via setting the `NGINX_ROOT` environment variable. This should be a relative path in your repository.

You may completely override the built-in nginx config by placing an `app-nginx.conf.sigil` file in the root, modeled after our own [`conf/app-nginx.conf.sigil`](https://github.com/dokku/buildpack-nginx/blob/master/conf/app-nginx.conf.sigil). This will be used inside of the container, and not by the host Dokku instance. See the [sigil project](https://github.com/gliderlabs/sigil) for more information concerning the sigil format.
