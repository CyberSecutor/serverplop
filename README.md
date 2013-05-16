#Serverplop

Server installation bundles and fixes. Adding lazyness to being a developer.

![http://www.allemaalleuk.nl/media/catalog/product/cache/1/thumbnail/50x/9df78eab33525d08d6e5fb8d27136e95/k/a/kabouter_plop_pak_-1.jpg](http://www.allemaalleuk.nl/media/catalog/product/cache/1/thumbnail/50x/9df78eab33525d08d6e5fb8d27136e95/k/a/kabouter_plop_pak_-1.jpg) Plopperdeplop

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