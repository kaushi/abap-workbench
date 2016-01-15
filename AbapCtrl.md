# Introduction #

This program demonstrate the processing of the control levels.

## Details ##

```
SORT i_tab BY matnr.

DATA : g_tab like LINE OF i_tab.

LOOP AT i_tab.
" Store the values of the current row before proceeding, 
otherwise the data will be lost."
    g_tab = i_tab.

    AT NEW matnr.
        WRITE: i_tab-matnr. " When new material code was found, Print the material code." 
    ENDAT.

    AT END OF matnr.
        ULINE.
    ENDAT.

ENDLOOP.
```