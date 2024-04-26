# This is the header

![JC](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/Jessica_Chastain_Cannes_2016_4_%28cropped%29.jpg/330px-Jessica_Chastain_Cannes_2016_4_%28cropped%29.jpg)


```
 \ Example 3.2

 INCLUDE "../../lib/constants.asm"
 screen = &7E40
 mode   = 6

 ORG &2000

 .start
     LDA mode
     JSR screenmode
     LDX #0
     LDY #0
     JSR tab
     LDA #15
     JSR printhex
     LDX #0
     LDY #1
     JSR tab
     LDA #&32
     JSR printhex
 .finish
     RTS
 .screenmode
     INCLUDE "../../lib/screenmode.asm"
 .printhex
     INCLUDE "../../lib/printhex.asm"
 .tab
     INCLUDE "../../lib/tab.asm"
 .end

 SAVE "MyCode", start, end

```
