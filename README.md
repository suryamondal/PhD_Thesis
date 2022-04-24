# My PhD thesis

The most important part is the bibliography, where most of us get confused.
The articles/books/notes are listed in the `chapters/surya_thesis.bib` file.

Bibliography file is compiled with `bibtex`, but there is a catch.
When we run `pdflatex` for the fist time, it creates a bunch of files where
the reference to the citations are stored. At this point, `pdflatex` has no
no idea how to fill those `?` positions. Then we run `bibtex`. It uses those
references to create a `.bbl` file. Then we run `pdflatex` again to fill the
`?`.

Relax, no need to get worried. It all have been taken care of in the `execute`.

One important advantage of `bibtex` is that it sorts the `bibitems`
automatically. So one does not need to take care of the ordering of items
in the `.bib` file when populating.

```
Compile with bibliography:  ./execute surya_thesis 1
                     Else:  ./execute surya_thesis
```

**Cover Page**: For book binding: This is given in `titlepageCover` directory.

Go to this directory and compile with: `pdflatex surya_thesis.tex`.
