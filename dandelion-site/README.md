Dandelion Site Docker image
================

This image is based on the official Jekyll Docker image: https://github.com/jekyll/docker-jekyll/blob/master/README.md

It only bundles additionnal gems required for the Dandelion site to run properly.

## Usage

    docker run --rm -v $(pwd):/srv/jekyll -p 4000:4000 dandelion/jekyll

Where `$(pwd)` points to the folder where the Jekyll site already exists.

***On Windows, ensure to execute the above command in the boot2docker VM.***