#Serverplop

Server installation bundles and fixes. Adding lazyness to being a developer.

![http://www.doosvolplezier.nl/media/catalog/category/1._cover_kabouter_plop.png](http://www.doosvolplezier.nl/media/catalog/category/1._cover_kabouter_plop.png)

## Ubuntu 13.04

To simply build a fresh development environment, do the following:

```
$ cd ubuntu-13.04
$ make development
```

Development is a bundle make rule for the following make rules:

- webserver
- phpunit
- java8
- nodejs
- square

`make nodejs` will also call for the `make java8` rule, which will install the Oracle version of Java version 8.
Please note that `make java8` will remove all `openjdk*` packages if you agree or frantically mash return.

### AMD Watermark fix
Additionally I personally encountered an issue with a huge ass watermark being planted on my monitors.
That watermark is meant for in-house testing purposes at AMD. You can remove it with a make rule.

```
$ sudo make amd-watermark-fix
```