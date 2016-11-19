postgresql93 homebrew formula
=============================

Homebrew-versions dropped support for it postgresql93 so I pulled the formula into this repo.

Usage
-----

```bash
$ brew tap jibberia/homebrew-postgresql93
$ brew install postgresql93
$ # for example:
$ brew services start postgresql93
```

Nightmare Hack Installation of PostGIS
--------------------------------------

Don't ever do this.

After installing postgis (`brew install jibberia/homebrew-postgresql93/postgis`), I didn't bother learning how to properly create Homebrew formulae and manually copied the PostGIs artifacts like so:

```bash
$ cp /usr/local/Cellar/postgis/2.3.0_1/include/* /usr/local/Cellar/postgresql93/9.3.14_1/include/
$ cp /usr/local/Cellar/postgis/2.3.0_1/lib/* /usr/local/Cellar/postgresql93/9.3.14_1/lib/
$ cp /usr/local/Cellar/postgis/2.3.0_1/share/postgresql93/extension/* /usr/local/Cellar/postgresql93/9.3.14_1/share/postgresql93/extension/
```

Again, don't ever do this.
