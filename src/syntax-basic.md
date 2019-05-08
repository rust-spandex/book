# SpanDeX syntax

The syntax of DeX is inspired by
[Markdown](https://en.wikipedia.org/wiki/Markdown) and, to a lesser
extent, by [elm-markup](https://github.com/mdgriffith/elm-markup).

## Paragraphs

In DeX, paragraphs are content that are not titles and that are separated
by an empty line.

``` md
This is a paragraph.
This is still the same paragraph.

This is a new paragraph.
```

## Titles

Titles are declared by prepending a line with `#`, just like Markdown.

For example, you may make titles and subtitles like so:

``` none
# My title

## My subtitle
```

In DeX, however, you need to leave an empty line following a title.

If you try to compile this

``` none
# My title
## My subtitle
```

the compiler will crash giving the following ouptut:

``` none
error: titles must be followed by an empty line
 --> main.dex:2:1
  |
2 | ## My subtitle
  | ^ expected empty line here
  |
```

## Inline

Like many markup languages, DeX has inline elements that allow you to
typeset your content. Inline elements cannot spread accross different paragraphs.
If you want to do that, you will have to end your inline at the end of your
paragraph, and start it again at the begining of the next one.

### Bold

To put some content in bold, you need to put it between stars (`*`). For
example, you can do:

``` none
This is a *strong* element.
```

As described previously, trying to spread an inline over different paragaphs
won't work, and the compiler will give an error saying that you haven't closed
your inline tag. For example, the following code

``` none
Hello *you

how* are you?
```

will give the following errors:

``` none
error: unmatched *
 --> main.dex:1:7
  |
1 | Hello *you
  |       ^ bold content starts here but never ends
  |
error: unmatched *
 --> main.dex:3:4
  |
3 | how* are you?
  |    ^ bold content starts here but never ends
  |
```

However, since pargraphs can spread over multiple lines, you can totally do the
following:

``` none
Hello *you.
How* are you?
```

### Italic

To put some content in italic, you neeed to put it between slashes (`/`). For
example, you can do:

``` none
This is an /emphasized/ element.
```
