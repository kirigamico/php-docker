# PHP

## Includes:

* PHP 5.6
* Apache
* Composer
* Node.js, npm
* bower, grunt, gulp (globally installed)

## How to use:

I made this to be used as a base image when creating your own project specific Dockerfile. Out of the box, you just `COPY` your code to `/app` and you're set.

### My document root isn't in my project's root

If your project is meant to be served _not_ from the root project folder, you need to modify the default VirtualHost. Get the `app.conf` file in the GitHub repo for this image, set `DocumentRoot` to _your_ document root, then replace the default `app.conf` file. `COPY app.conf /etc/apache2/sites-available/app.conf`.

### Other setup

This image is meant to be used as a base image. Other things like installing node and bower dependencies is something you should configure yourself in your Dockerfile.
