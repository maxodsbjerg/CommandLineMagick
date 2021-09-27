# CommandLineMagick

Fede oneliners og scripts


## Copy files returnet from ls

`ls | egrep 'Skærm.+\.png'| xargs -I '{}' cp '{}' ~/Documents/workspace/2021/image_mosaic/pic/screenshots`
