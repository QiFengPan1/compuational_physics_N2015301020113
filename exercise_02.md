# Exercise_02
```python
#TO SHOW STRING "PQF!" IN THE WINDOWS CONSOLE
import os
import time
#windows console width
width = 57
#
printedMessage = ["###########           ############           ############",
                  "##       ##          ##          ##          ##          ",
                  "##       ##          ##          ##          ##          ",
                  "##       ##          ##          ##          ##          ",
                  "###########          ##       ## ##          ########### ",
                  "##                   ##         ###          ##          ",
                  "##                   ##          ###         ##          ",
                  "##                   ##          ## ##       ##          ",
                  "##                    ############   ##      ##          ",]
#
offset = width
#
while True:
    os.system("cls")
    for row in range(9):
        print(" " * offset + printedMessage[row][max(0,offset*-1):width - offset])
        #
    offset -= 1
    if offset <= len(printedMessage[0]) * -1:
        offset = width
    #
    time.sleep(0.075)
    #
