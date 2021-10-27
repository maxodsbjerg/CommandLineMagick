# CommandLineMagick

Fede oneliners og scripts

## Manipulate results from ls

I de første to commands herunder er `-I` the name of the game. Den får xargs til at newline som seperator mellem inputs i stedet for whitespace. Hvilket er noget rod, når der er mellemrum i filnavnet. 

### Copy files returnet from ls

    ls | egrep 'Skærm.+\.png'| xargs -I '{}' cp '{}' ~/Documents/workspace/2021/image_mosaic/pic/screenshots`
    
### Remove files from ls 
    ls | egrep 'Skærm.+\.png'| xargs -I '{}' rm '{}'


## Batch process files in OCRmyPDF:
    parallel --tag -j 2 ocrmypdf -l dan+eng '{}' '{}' ::: *.pdf

## Combinging several pdfs into one using qpdf

    qpdf --empty --pages *.pdf -- out.pdf`
    
## Create PDF as A4 paper from jpg and jpeg files
    img2pdf --pagesize A4 *.jp* --output test.pdf
    
## Ghostscript command to compress pdf-files
    gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/printer -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
