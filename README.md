
# Deffy_AppImage

 - Deffy + Wine

Deffy converts DFF files (either containing DSD or DST) to DSF files or converts DSF files to DFF files

https://www.mymymyohmy.com/software/deffy.html

## Repository: https://github.com/ryuuzaki42/Deffy_AppImage
    Deffy: 6.0.1

---
## Using Wine in AppImage from https://github.com/mmtrt/WINE_AppImage - Stable 
### Change made:

#### Remove 32 bits
    cd opt/wine-stable/lib/wine/
    rm -r i386-windows/

#### Disable core fonts download/instal
    ... WINEDLLOVERRIDES="mscoree=d;mshtml=d" ...

#### Prefix in RAM - zero disk footprint
    folder_name_RAM="Deffy_AppImage_$(date +%d_%m_%Y)"
    mkdir -p /dev/shm/$folder_name_RAM/
    ... WINEPREFIX=/dev/shm/$folder_name_RAM ...
    rm -r /dev/shm/$folder_name_RAM/

---
https://www.mymymyohmy.com/software/deffy.html#download
