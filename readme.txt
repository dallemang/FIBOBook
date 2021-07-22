
    Use TexLive 2014 or later that is free from tug.org,
    or use another compatible version of LaTeX


    Please see

        fm.tex
            - please modify the fm.tex file to show the
                the book title
                the authors' names
                the authors' affiliations
                the abstract and keywords
                the table of contents
                an optional preface
                an optional acknowledgements


        book.tex
            - it is a sample driver program
            - use this file to set up the list of files for your book
            - we will produce the front matter for your book

            - use
                \usepackage{morgan2}
                morgan2.sty has the M&C Publishers macros

                \usepackage{natbib}
                natbib.sty supports the Author-Year or numerical style
                for the bibliography (more later)

                \usepackage{morgan-defs}
                to bring the necessary style files and define a number
                of macros we use in the production of your books


        ch01.tex
            - use one file per chapter, please
            - look for \begin{figure} to find

                \begin{figure}[hbt]
                \includegraphics[width=3.3in]{line-spaces.eps}
                \caption{Communication system block diagram.}
                \label{ch01.fig1}
                \end{figure}

            - look for \begin{table} to find out how to create a
              table WITH a \caption and use colors for the rows
              instead of using \hline that Adobe Reader does not
              display well

            - look for \begin{tabular} to find out how to create a
              table WITHOUT a \caption and use colors for the rows
              instead of using \hline that Adobe Reader does not
              display well

            - if you wish to have an index in your books, you
              will need to insert entries of the form

                \index{term to appear in index}%

              and we will produce an index using your entries
              of the type above.
              The \index{...}% should appear by itself in a
              line and it should terminate with a % to avoid
              generating extra spaces in your book.

              Please see the \index{...} entries in the files
              ch01.tex and ch02.tex. If you wish to create an
              index, you'll need the command \makeindex in the
              preamble (before \begin{document}).

              You then need to run LaTeX on book.tex. Because
              of the command \makeindex, you'll get a book.pdf
              as usual, and, this time you'll also get a file
              called book.ind. Then you need to run makeindex:

                makeindex  book

              The utility makeindex looks for a file called
              book.idx and then produces another file called book.ind

              Please see the book.tex where, after we produce
              the book.ind file, we produce the index. Make
              sure that

                \input{book.ind}

              is commented out (i.e., it is preceded with a %)
              until you produce the book.ind file. You may also
              want to look at another file called book.ilg for
              any illegal commands you may have in your .tex files.

              If you have access to "Guide to LaTeX," fourth
              edition, by Kopka and Daly, take a look at pages
              222 through 226. It is an excellent book.

        ch03.tex
            - an example an Algorithm

        ch04.tex
            - using shaded areas

        ch05.tex
            - using bold math

        ch06.tex
            - please read the contents on Chapter 6 (one page)
              in book.pdf to see how one uses the "Author-Year"
              type of bibliography; for that to work one needs
              to say

                \usepackage{natbib}

              as it appears in book.tex


        biblio.tex
            - see how to create your bibliography using the
              "Author-Year" style;

            - if you use .bib, please send us the .bbl file that
              BibTeX generated for you; it is often helpful to have it


        book-Clibre.pdf
            - this file contains the results of running book.tex
              and generating a pdf file using Caslon Libre fonts (default).


        book-Times.pdf
            - this file contains the results of running book.tex
              and generating a pdf file Times fonts; see \morgansetup
              in book.tex.


        please see the following folders:

            abs-pref
                samples of Abstracts and Prefaces that appears in
                other M&C books

            bios
                samples of short bios; photos are optional

        requests:
            -   please start a new line whenever you use a period to end a
                sentence. That could avoid some tools limitations on the
                length of a single line

            -   please end the figure captions with a period

            -   please do not use a period in table captions

            -   commas:
                    -   please a comma after i.e. and e.g.

                    -   please use a comma before "and" in a series of
                        three or more terms; e.g., "copper, silver, and gold"

        About an Index:
            - if you wish to create an index for your manuscript, please
              consult "Guide to LaTeX," 4th edition, by Kopka and Daly,
              pages 222-225

            - other sources for Indexing in LaTeX:

                https://en.wikibooks.org/wiki/LaTeX/Indexing

                http://www.pctex.com/files/managed/3/3a/makeindx.pdf

                http://www.math.utah.edu/~beebe/talks/1998/idxtips.pdf

                https://www.youtube.com/watch?v=HwjSkupEgIo


    If you come across problems or have specific questions, please send
    us a short .tex file that shows the problem and we'll try go get you
    an answer. We'll assist you in creating nice looking books for M&C.

    Please contact us at

                drtondo@t3works.com

