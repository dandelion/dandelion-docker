Dandelion Site Docker image
================

## Usage

    docker run --rm -v $(pwd):/srv/jekyll -p 4000:4000 dandelion/jekyll

Where `$(pwd)` points to the folder where the Jekyll site exists.