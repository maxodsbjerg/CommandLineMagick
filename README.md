# CommandLineMagick

Fede oneliners og scripts

### Batch process files in OCRmyPDF:
    
    parallel --tag -j 2 ocrmypdf -l dan+eng '{}' '{}' ::: *.pdf
    
