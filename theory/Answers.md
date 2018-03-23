
* Single regex that matches either of these:

    antelope rocks out
    antelopes rock out

* /antelopes?/g

* Regex that matches either of:

    goat
    moat

  but not:

    boat
* /[g,m]oat/g

* Regex that matches dates in YYYY-MM-DD format. (Year can be 1-4 digits, and
  month and day can each be 1-2 digits). This does not need to verify the date
  is correct (e.g 33333-33-33 can match).

  2000-10-12
  1999-1-20
  1999-01-20
  812-2-10
* /\b\d{1,4}(-\d{1,2}){2}\b/



* The VT-100 terminal (console) outputs text to the screen as it
  receives it over the wire. One exception is that when it receives an
  ESC character (ASCII 27), it goes into a special mode where it looks
  for commands to change its behavior. For example:

      ESC[12;45f 

  moves the cursor to line 12, column 45.

      ESC[1m

  changes the font to bold.
* ESC[1m --- /(?<=ESC\[)\d(?=[a-z])/. This regex will accept only '1' after checking if ESC[ precedes the '1' and a letter precedes it.
*  ESC[12;45f ----/(?<=ESC\[)\d+;\d+(?=[a-z])/ will select line and column value in form 12;45. Split at ';' to get arr of [line,column]
