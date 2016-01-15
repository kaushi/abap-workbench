# Introduction #

The process of creating and adding a new holiday to holiday and factory calendar is described here.


### SAP Calendar Master ###

**Public holidays:** can be defined and be combined into holiday calendars.

Public holidays describe the statutory holidays for a particular country or region within a country.

Types of Public holidays:
  * Fixed date
  * Fixed day of week from a specific date
  * Specific number of days before or after Easter (Sunday)
  * Easter Sunday
  * Moveable holiday (with individual specification of dates during each specified year).
For holidays with fixed date (such as Christmas) and moveable holidays it is possible to specify simple rules guaranteeing the holiday if it falls on certain days of the week (Thu, Fri, Sun, Sat/Sun). For instance, Christmas day public holiday may be moved to the next working day if it falls on a Saturday or Sunday.

**Holiday calendar:** assigned to each factory calendar.

**Factory calendar:** contain company specific dates such as alternate working Saturdays and holidays.

<a href='https://picasaweb.google.com/lh/photo/rNL1Yd_U0zhYB2i-p46fW-nxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh3.googleusercontent.com/-TVwthuOZ0fM/TugxhUbxGfI/AAAAAAAACLQ/2rowy7hyxiM/s288/scal0.PNG' height='288' width='237' /></a>

_IMG SPRO -> Time Management -> Work Schedules_

_T-Code **SCAL**_

#### Step 1: Create Public Holidays ####
<a href='https://picasaweb.google.com/lh/photo/MXn8J3SZlfjNwJsvR5gXBenxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh4.googleusercontent.com/-0EtsK7UonL0/Tug9JJLvFbI/AAAAAAAACLo/nWL-q6t9OxA/s400/scal_pub0.PNG' height='400' width='327' /></a>
  1. Select the radio button _Public holidays_.
  1. Click _Change_ button <a href='https://picasaweb.google.com/lh/photo/D0j4bEaGkM-vFRrHkLPUd-nxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh5.googleusercontent.com/-lgNRhyx6Hs8/Tug7OxGRYqI/AAAAAAAACLY/bwIHi7V5vYo/s800/edit.PNG' height='21' width='21' /></a>.
  1. On _Change Public Holidays: Overview_ screen click _Create_ button <a href='https://picasaweb.google.com/lh/photo/u-JCkcyDJqYboHoslS5xd-nxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh5.googleusercontent.com/-dsKTPcn1nhU/Tug9u2X1FrI/AAAAAAAACLw/EI5FFkbG7I0/s800/create.PNG' height='21' width='20' /></a>.
  1. A pop up window appear to select the _Type of Public Holiday_.

<a href='https://picasaweb.google.com/lh/photo/p25l0JodFQNtMGXQALBAWunxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh4.googleusercontent.com/-JPptjoKJ56w/TuhHmSeO4rI/AAAAAAAACL4/eV1IfhH_XZk/s400/scal_pub_fix0.PNG' height='334' width='400' /></a>

**_Type of Public Holiday_**
  1. with fixed date: This public holiday falls on the same date every year. (e.g. Christmas Day).
    * Enter the _Public Holiday Definition_.
      * Day (e.g. 25)
      * Month (e.g. 12)
      * _Guaranteed_ : specify whether the public holiday should be moved or not if it falls on a weekend.
        * Not Guaranteed: Indicates that the public holiday should not be moved if it falls on a weekend.
        * Thursday, Friday, Sunday, Saturday/Sunday: If the public holiday is to be "guaranteed", i.e., should be a day off in any case, you have to specify the workday to which the public holiday should be moved.
    * Enter the _Public Holiday Attributes_
      * Sort Criterion: use this to display logically related holidays in a block, e.g. all holidays for a country.
      * Religious Denomination: (e.g. Christianity).
      * Public Holiday Class: this specifies the holiday type. It can be used to determine the groups of holidays and normal days. (e.g. '1' is ordinary public holiday).
      * Give Long/Short Holiday Names.
    * Click _Create_ icon <a href='https://picasaweb.google.com/lh/photo/u-JCkcyDJqYboHoslS5xd-nxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh5.googleusercontent.com/-dsKTPcn1nhU/Tug9u2X1FrI/AAAAAAAACLw/EI5FFkbG7I0/s800/create.PNG' height='21' width='20' /></a>.
  1. Floating Public Holiday: This public holiday is not fixed. It must be defined explicitly each year. (e.g. Vesak Full Moon Poya Day).
    * Enter the _Public Holiday_ into relevant boxes: Year/Month/Day (e.g. 2012, 05, 05).
    * Enter the _Public Holiday Attributes_ and click _Insert Date_ icon.

<a href='https://picasaweb.google.com/lh/photo/xWQdl_mOOyv7C7BSiBMZTOnxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh5.googleusercontent.com/-NsA2dmsfwUs/TuhJP-Z1kJI/AAAAAAAACMA/1Q4Swru_k9A/s400/scal_pub_float.PNG' height='398' width='400' /></a>

#### Step 2: Create Holiday Calendar ####

Insert public holidays in holiday calendar.
  1. Select the radio button "Holiday Calendar".
  1. On _Change Public Holiday Calendar: Overview_ screen click _Create_ button <a href='https://picasaweb.google.com/lh/photo/u-JCkcyDJqYboHoslS5xd-nxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh5.googleusercontent.com/-dsKTPcn1nhU/Tug9u2X1FrI/AAAAAAAACLw/EI5FFkbG7I0/s800/create.PNG' height='21' width='20' /></a>.
  1. Enter the Calendar ID and the Name of the calendar.
  1. Enter the validity of the calendar.
  1. Click on the _Assign Holiday_ button to assign the holiday.
<a href='https://picasaweb.google.com/lh/photo/IS3a_hufbYJuzC4eKml1WunxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh4.googleusercontent.com/-2zHqX98moKc/TuhUJxXAv_I/AAAAAAAACMI/TozB0S31I9k/s400/scal_holi_cal.PNG' height='400' width='368' /></a>
  1. From the _Insert Public Holidays into Holiday Calendar_ screen, search for the respective calendar and select the holidays you want to allow.
  1. Click on the _Assign publ.holiday_ Button.
  1. The public holiday gets added; click on save button to save the holiday calendar.
  1. Acknowledge all the messages.

<a href='https://picasaweb.google.com/lh/photo/6Cjdf0qtnlT2ERS5i9-0sunxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh4.googleusercontent.com/-bw9LYjwuuyY/Tuhby01M47I/AAAAAAAACMc/UfhCnEfxW_8/s288/scal_pub_holidays.PNG' height='288' width='229' /></a>

#### Step 3: Define the Factory Calendar ####

Select the working days and assign a holiday calendar to factory calendar.
  1. Select the radio button "Factory Calendar".
  1. Enter the Factory Calendar ID (same as the Holiday Calendar) and the Factory Calendar Name.
  1. Enter the Holiday Calender ID.
  1. Save.
  1. Click _Year Overview_ and check for the dates.

<a href='https://picasaweb.google.com/lh/photo/sF47M8SzweF3nI8EYH123OnxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh6.googleusercontent.com/-LNGFQlBu5tU/TusfD5l_WRI/AAAAAAAACMo/847GE-dehl8/s400/scal_year_view.PNG' height='348' width='400' /></a>

#### Final Step: Transport the Calendar ####

  1. Go to _SAP Calendar: Main Menu_
  1. Select one of the subobjects and click _Transport_ button <a href='https://picasaweb.google.com/lh/photo/xmSqlTEh54-HQOSwqg-Fp-nxGx3DgLdBjDtHO-Szlzw?feat=embedwebsite'><img src='https://lh6.googleusercontent.com/-VVMToO3Tpx0/Tusf3qE0DgI/AAAAAAAACMw/puVRzw_Ws7E/s800/transport.PNG' height='21' width='20' /></a>.

