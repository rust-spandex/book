# Introduction

Welcome to the SpanDeX book. This book serves as a tutorial for SpanDeX.

## What is SpanDeX?

SpanDeX is a modern alternative to LaTeX, carefully designed to be:

- **ultra performant**, allowing lightning fast compilation and
  hot reloading with optimized algorithms;
- **simple**, avoiding the need for users to learn a complex
  language before being able to do basic things;
- **easy to debug**, not reproducing the tons of useless stuff LaTeX vomits
  every time something goes wrong and making it a breeze to find and fix simple
  mistakes.

## Main TeX's pitfalls being worked on

Overall, SpanDeX aims at taking advantage of TeX's strengths while proposing
novel approaches where it performs poorly. The core idea behind SpanDeX is to
build things in a way that will allow the engine to take smarter decisions at
every step.

### TeX's opaque syntax

While nearly every academic paper involving some level of math is written in
TeX and people became accustomed to it, its syntax can be quite a challenge to
grasp for the newcomer.

For instance, though it's pretty straightforward to typeset basic paragraphs and
titles in TeX, it becomes extremely unhandy and clogged up with avoidable stuff
as soon as you'd like to stylize your document somewhat.

DeX proposes to instead invest on what's been done with the most recent
languages that aim at being minimalistic while remaining explicit and easy to
remember.

### TeX's unability to typeset paragraphs in a fully context aware manner

TeX does not keep track of where it is when it tries typesetting paragraphs.
This makes it nearly impossible to implement somewhat complicated layouts in a
straightforward way. Moreover, this prevents TeX's core typesetting algorithm
from having the opportunity to take smarter decisions when breaking down
paragraphs into lines, /e.g/ to avoid orphans and widows.

SpanDeX implements a novel approach based on the concept of layouts. In this
paradigm, a paragraph "typesets itself" inside of a layout that tells the
paragraph where it is and where it can go next. This gives the paragraph the
possibility to make smart decisions and even go back, if necessary. Being
context-dependent, this approach also unveils opportunities for improved caching
and thus, performance.

It then becomes extremely simple to define and configure arbitrary layouts,
dissect them into columns, etc.

## WIP

This project is still very recent, and very (very) few functionnalities are
supported. This is not production ready in any way, it's simply here if you
want to have fun and play around.

## API documentation

The API documentation is available [here](/spandex).

## Source code

[The source code is available on GitHub](https://github.com/rust-spandex/spandex).
