# Drawing-with-Metapost

This project provides a document that discusses how to draw technical diagrams
with John Hobby's Metapost language. It includes over 200 illustrations
created with Metapost, complete with source code as inspiration and examples.
The intended level is for intermediate to advanced users rather than complete
beginners.  For introductions, tutorials, and other articles about Metapost,
see http://www.tug.org/metapost.html

Start with "Drawing-with-Metapost.pdf" in the top directory.

The `src` directory contains 
- the TeX source for the main document
- the style file used for marking up Metapost source code
- the Metapost source for each illustration used in the main document
- the corresponding PDF file created from the MP source

You might like to read the main document first, but you might also like to
browse through the PDFs in the src directory, and when you find one that is
interesting, have a look at the corresponding MP source file.  There is a
one-to-one match between the PDF names and the MP source names, so
"apollonius.pdf" is created from "apollonius.mp".  The src directory contains
a few drawings that are not (yet) included in the main document.

To update the main PDF document I follow these steps

- build any new or updated Metapost source files with `lualatex` to create PDFs in the src directory
- build the main tex file with `lualatex -output-directory=.. -recorder Drawing-with-Metapost`
- run a Python script to read the .fls and `git add` all the files used
- git commit and push

Toby Thurston -- 08 May 2024

Copyright (c) 2024 by Toby Thurston. This material may be distributed only
subject to the terms and conditions set forth in the Open Publication License,
v1.0 or later (the latest version is presently available at
http://www.opencontent.org/openpub/).
