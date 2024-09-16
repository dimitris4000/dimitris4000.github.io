
# File structure
 - *public* This directory is completely generated and contains all the static code required for the site to run after build. Feel free to delete and recreate by regenerating the site with `hugo` command (see "How to build production" section)
 - *docs* This is a symlink to the `public` directory. It is required because this is the directory Github pages reads to serve the page.

# How to build production
HUGO_ENV="production" hugo
