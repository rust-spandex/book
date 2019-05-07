# Installing SpanDeX

SpanDeX is not (yet) tested on any other operating system other than Linux
based.

## Install rust

The first thing you need to do in order to run SpanDeX is to install rust.
If you're on a Linux based system, it should be as simple as running

``` bash
curl -sSf https://sh.rustup.rs | sh
```

in a terminal and answer the few questions that will be prompted.

If you're on another operating system, we invite you to [read rust's
documentation](https://doc.rust-lang.org/book/ch01-01-installation.html) to
find out the best way of installing rust on your computer.

## Install SpanDeX

If you have successfully installed rust, you should be able to install SpanDeX
by simply running

```
cargo install --git https://github.com/tforgione/spandex -f
```

You can run this command again to update SpanDeX to the latest version.

