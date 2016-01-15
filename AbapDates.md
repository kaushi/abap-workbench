# Introduction #

This program guides you how to manipulate the ABAP data structure of the system date type.

## Details ##

Date variables of type `sy-datum` are stored in a standard table.

We could define the date variable as follows:
```
SELECT-OPTIONS : s_date FOR sy-datum NO-DISPLAY. 
```

`sy-datum` has the following structure:

  * Sign - Character type length 1.
  * Option - Character type length 2.
  * Low - Date type length 8 (start date)
  * High - Date type length 8 (end date)

For example: Date range between 2011.01.01 to 2011.12.31 will be stored in `s_date` variable as follows.

`IBT2011010120111231`

The structure for the `s_date` would be:
| SIGN | OPTION | LOW | HIGH |
|:-----|:-------|:----|:-----|
| I	   | BT     | 20110101| 20111231 |

If you want to modify the date object, move each field individually, then modify and append to the structure.

```
    MOVE : 'I' TO s_date-SIGN.
    MOVE : 'BT' TO s_date-option.
    MODIFY s_date.
    APPEND s_date.
```