Regular expression - reference

Anchors -> where a match should occur
^regex – beginning of line
regex$ - end of line
eg ^dog$ -> will search a line which dog, if testdog or dogtest will not show
 ? -> if next letter matches or not. Eg s?o will search s or so
\<refex – beginning of a word
Refex\> - end of a word
Eg th\> à all word that end with th such as with, both will show up 
OR 
\<th à all word that start with th such as the, that will show up
. à can represent anything eg, c.t can be cat,cut,c5t etc
* à represent zero or more character which can even include spacing eg, c.*t , means ‘c’ followed by 0 or more ‘.’(which means anything) followed by ‘t’ . Can be ct, cat , concat , cot , clatter coot . last example is correct because start with c and end with t eventho there is space in between
[auo] à can represt any of the letter inside [], eg c[aou] can be cat,cut,cot
Eg of complex sample  à c.[auo]t -> can be clot ,clat, coot, cout etc…
Eg of complex sample à ^[cC]at -> all line that start with cat or Cat
Eg of complex sample à ca*t -> this means ‘c’ followed by 0 or more ‘a’ followed by ‘t’ . can be caaaat, ct, cat
Eg of complex sample à c[aou]*t -> this means ‘c’ followed by 0 or more ‘a’  or ‘o’ or ‘u’ followed by ‘t’ . can be caaaat, ct, cout, coat, cut 
 
.\{2\} àCan use braces to limit number to 2 but need to use escape character 
eg c.\{2\}t -> this means ‘c’ followed by exactly 2 characters followed by ‘t’ . can be coat, caat , catt, coot, cout 
eg co\{2\}t -> this means ‘c’ followed by exactly 2 ‘o’ followed by ‘t’ . can be coot only
eg c[aou]\2{2\}t -> this means ‘c’ followed by exactly 2 (‘a’ or ‘o’ or ‘u’). can be coat ,coot, cout
