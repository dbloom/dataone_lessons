Thank you for contributing to the material! This document provides an
introduction to the ways the lessons are organized, the tools we use to render
them, and the type of modifications we expect.

# Guidelines for contributors and content editors

The lessons are generated from markdown documents. These guidelines will walk
you through the repository organization, the markdown basics, and any additional
information.

## Repository organization

Every lesson is a single folder within the `lessons` directory. Each lesson
folder is called `XX_keyword`, where `XX` is the lesson number, and `keyword` is
a brief description of the lesson. The slides themselves are in a file called
`index.md`. Do not use another filename. For example, the [demonstration
lesson][demolessonhtml] markdown file can be [viewed here][demolessonmd]. This
demonstration lesson showcases most of the features you can use in your slides.

[demolessonhtml]: https://dataoneorg.github.io/Education/lessons/00_markdown/index.html "Rendered demonstration lesson"
[demolessonmd]: https://github.com/DataONEorg/Education/blob/master/lessons/00_markdown/index.md "Raw markdown file for the demonstration lesson"

You are free to add other directories to your lesson. Images go in `images`, and
PDF files in `pdf`. For example, a lesson repository could look like:

~~~
01_management/
  index.md
  images/
    image1.png
    image3.jpg
  pdf/
    one-pager.pdf
~~~

## Informations about the tools used

The markdown documents are rendered into a website using [*Jekyll*][jekyll]. The slides
themselves are rendered using [*remarkjs*][remark]. The rendering is done using github
pages, which builds the site from the `master` branch. You can build the site
locally with `jekyll serve -w`, and it will be available at
[`http://localhost:4000`][local] for you to review.

[jekyll]: https://jekyllrb.com/ "Jekyll website"
[remark]: https://remarkjs.com/#1 "RemarkJS website"
[local]: http://localhost:4000

The stylesheets are defined in `resources/styles`, and rendered to
`resources/dataone.css` using `lessc` (just type `make` from the root).

## How to contribute

### Adding content

1. Create a fork of the repository into your github account
2. Modify the files that you want to change
3. Submit a pull-request against the `master` branch of this repository
4. Your changes will be reviewed

### Suggesting changes

1. Open an [*Issue*][issue] on this repository.

[issue]: https://github.com/DataONEorg/dataone_lessons/issues

### Page not rendering?

Check that the `title` field of the YAML header (the first line of each
lesson) is in quotes.
