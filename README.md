# MkDocs as Personal Page

Using [Material for MkDocs](https://github.com/squidfunk/mkdocs-material) as Personal Page.

## Quick start

Material for MkDocs can be installed with `pip` (probably you can also use `virtualenv`):

```bash
pip install -r requirements.txt
```
To preview the Personal Page locally, you can run:
````bash
mkdocs serve -a 0.0.0.0:8000
````
And then have a look in the browser at the [page](http://localhost:8000).

## Deploy with GitHub pages

Just run the command:
````bash
mkdocs gh-deploy
````