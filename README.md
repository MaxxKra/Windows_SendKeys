# Windows_SendKeys
Eine Liste von Tastenbefehlen welche per MQTT an meinen Windows PC gesendet werden können.


| **TASTE** | **CODE** |
| --- | --- |
| BACKSPACE | {BACKSPACE}, {BS}, or {BKSP} |
| LEERTASTE | ( ) |
| CAPS LOCK | {CAPSLOCK} |
| ENTFERNEN oder Entf | {DELETE} or {DEL} |
| EINFÜGEN oder Einfg | {INSERT} or {INS} |
| ESC | {ESC} |
| ENTER | {ENTER} or ~ |
| PFEIL LINKS | {LEFT} |
| PFEIL OBEN | {UP} |
| PFEIL UNTEN | {DOWN} |
| PFEIL RECHTS| {RIGHT} |
| ENDE | {END} |
| HILFE | {HELP} |
| BILD UNTEN | {PGDN} |
| BILD OBEN | {PGUP} |
| TABULATOR | {TAB} |
| F1 | {F1} |
| F2 | {F2} |
| F3 | {F3} |
| F4 | {F4} |
| F5 | {F5} |
| F6 | {F6} |
| F7 | {F7} |
| F8 | {F8} |
| F9 | {F9} |
| F10 | {F10} |
| F11 | {F11} |
| F12 | {F12} |
| NUM LOCK | {NUMLOCK} |
| Nummernfeld PLUS | {ADD} |
| Nummernfeld MINUS | {SUBTRACT} |
| Nummernfeld MULTIPLIZIEREN | {MULTIPLY} |
| Nummernfeld DIVIDIEREN | {DIVIDE} |


Um Tasten in Kombination mit einer beliebigen Kombination der Tasten UMSCHALT, STRG und ALT anzugeben, stelle dem Tastencode einen oder mehrere der folgenden Codes voran. 


| TASTE | CODE |
| --- | --- |
| UMSCHALT Shift | + |
| STEUERUNG Strg | ^ |
| ALT | % |


Um anzugeben, dass eine beliebige Kombination aus UMSCHALT-, STRG- und ALT-Taste gedrückt gehalten werden soll, während mehrere andere Tasten gedrückt werden, schließen Sie den Code für diese Tasten in Klammern ein. Um beispielsweise anzugeben, dass die Umschalttaste gedrückt gehalten werden soll, während E und C gedrückt werden, verwenden Sie „+(EC)“. Um anzugeben, dass SHIFT gedrückt gehalten werden soll, während E gedrückt wird, gefolgt von C ohne SHIFT, verwenden Sie „+EC“. 

Ich habe festgestellt, dass es mit dem deutschen Tastaturlayout Probleme gibt das Zeichen `^` als Text per SendKeys zu übertragen.
Eine Möglichkeit dies zu umgehen ist, das Tastaturlayout auf Englisch umzuschalten. Dazu habe ich ein zweites Tastaturlayout in Windows installiert und mit einem Shortcut zum Umschalten ( ALT+SHIFT ) versehen.

Um nun das Zeichen `^` als Text zu senden, habe ich folgende Verkettung von Keys vorgenommen:

`%(+){^}%(+)`

Mit dieser Kombination wird das Layout auf englisch umgeschaltet, dass Zeichen `^` geschrieben und das Layout wieder zurückgestellt.
Ohne diesen Workaround würde anstatt `^` immer `&` geschrieben.
