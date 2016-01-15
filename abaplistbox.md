# Introduction #

This code guide you how to fill a listbox with customized values.


## Demo ##

This example demonstrate adding a listbox with months from 'January' to 'December' to your screen.

First you need to define the List:
  * example:

```
  TYPE-POOLS: VRM.
  
  DATA: NAME TYPE VRM_ID,
        LIST TYPE VRM_VALUES,
        VALUE LIKE LINE OF LIST.
```

Then you need to add the screen element:

  * example:

```
  PARAMETERS: PS_MONTH(10) AS LISTBOX VISIBLE LENGTH 12.
  
  AT SELECTION-SCREEN OUTPUT.

    NAME = 'PS_MONTH'.
    VALUE-KEY = '01'.
    VALUE-TEXT = 'January'.
    APPEND VALUE TO LIST.

```

Finally, call the pre-defined function to fill the Listbox.

```
CALL FUNCTION 'VRM_SET_VALUES' EXPORTING ID = NAME VALUES = LIST.

```

### Final Output ###
![http://lh5.googleusercontent.com/-ug61MYpxk90/ThFD2VFCAOI/AAAAAAAACII/PfXOomcScmw/abaplistbox-1.png](http://lh5.googleusercontent.com/-ug61MYpxk90/ThFD2VFCAOI/AAAAAAAACII/PfXOomcScmw/abaplistbox-1.png)

_Give us some feedback_

