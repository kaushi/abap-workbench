# Introduction #

This program guide you how to auto-refresh your ABAP report without using the Dynapro utility.


## Details ##

First define the refreshing time of your report.

The function `Z_ENQUE_SLEEP` will enable you to set the program to sleep during the required time period.

```
FUNCTION Z_ENQUE_SLEEP.

DATA: ZTIME LIKE SY-UZEIT.
GET TIME.
ZTIME = SY-UZEIT + 30.

DO.
  GET TIME.
  IF SY-UZEIT >= ZTIME.
     EXIT.
   ENDIF.
ENDDO.

ENDFUNCTION.
```

`START_REFRESH` subroutine initiate the refreshing function.

```
FORM START_REFRESH USING TASKNAME.
" The SET USER-COMMAND initiates the communication back to the program"
  SET USER-COMMAND 'REFR'.
ENDFORM.
```

Then call `Z_ENQUE_SLEEP` to perform the `START_REFRESH` subroutine.
```
CALL FUNCTION 'Z_ENQUE_SLEEP'
   STARTING NEW TASK 'IF'
   PERFORMING START_REFRESH ON END OF TASK.
```

Finally, add the user command `REFR` to `AT USER-COMMAND` event.
This allows your program to react to refresh action triggering the `START_REFRESH` task.

```
AT USER-COMMAND.
IF SY-UCOMM = 'REFR'.
   SY-LSIND = SY-LSIND - 1.
   ADD 1 TO ZNUM.
   GET TIME.
ztime = sy-uzeit.
```