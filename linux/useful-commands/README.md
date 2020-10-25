# Useful-commands

* #### To get some information about a command?
    `$ curl cheat.sh/[command-name]` 

* #### PDF operations
    * Extract a range of pages
        `$ pdftk input.pdf cat [first_page]-[last_page] output output.pdf`
    * Merge $n$ PDFs
        `$ pdftk PDF1.pdf ... PDFn.pdf cat output merged.pdf`
    * Put multiple pages into one
        `$ pdfjam input.pdf --nup [col]x[row] --no-landscape --outfile output.pdf`
    * Convert PDF into grayscale
        ```
        gs\
            -sOutputFile=output.pdf \
            -sDEVICE=pdfwrite \
            -sColorConversionStrategy=Gray \
            -dProcessColorModel=/DeviceGray \
            -dCompatibilityLevel=1.4 \
            -dNOPAUSE \
            -dBATCH \
            input.pdf
        ```