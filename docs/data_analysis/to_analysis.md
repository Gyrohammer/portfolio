# Tiger Optics Analysis via Python
This is the batch monitoring that is mentioned on the previous page. Here I will be delving into more detail about the analysis and providing some censored visual examples.

Using a variety of libraries, including matplotlib, tkinter, and numpy, I created a program to quickly analyze data files for my job. I thought this necessary after I saw how data was initially processed: manually sifting through csv sheets and plotting. Not only was this previous method error prone (typing in functions manually), it was also slow and inefficient. 

## Initial Steps
#### VBA
My first foray into solving this inefficieny was via VBA (Visual Basic Analysis). I created a macro to automatically plot, display, and analyze the data in a given workbook. This method, while more consistent, was much less efficient with larger files (some files extend into the 200MB range). I attempted to optimize this macro to the best of my ability, but it was simply too slow for it to be useful. Transferring the macro from one user to another was also tricky, meaning any updates I made would require a Read Me to explain the process.

```
Sub TauMedMac_2_7()
'
' The Tau Med Mac (TMM) is a macro that assist in quickly visualizing plots for
' analysis.
' v2.6a
' - Total run time is now displayed in the top left of the workspace.
'
' v2.7
' - File run time now displays the _actual_ total runtime instead of resetting at 24.
' - Macro run time is now recorded and displayed.



With Application
.ScreenUpdating = False
.Calculation = xlCalculationManual
.EnableEvents = False
End With

Continued...
```

### Python
I then looked to some of the programming languages. I have some experience in C++ and Java, but found the libraries I would need to use difficult to operate and cumbersome to program. I needed something faster that could be written faster in a language that is new-user-friendly. That led me to Python. I had little to no experience programming in python before I began this journey. With every feature request and change comes new oppurtunity to learn and optimize. Along this journey I have become familiar with git and github as well as tracking changes, merging branches, all that fun stuff. 

```
# Author: Max Young
# Purpose: This program is used to analyze srda files generated by **** units.  This analysis includes
# visualized plots and automatic calculations for individual specifications. All of which are displayed
# to the user.
# Version: 4.5.1
import gc
import tkinter.messagebox as tkmb
import matplotlib
import matplotlib.pyplot as plt
from matplotlib.widgets import CheckButtons, SpanSelector
import numpy as np
import pandas as pd
import PySimpleGUI as sg
import re
import time

matplotlib.use('TkAgg')

layout = [[sg.Text('File Path: '), sg.Input(key='-IN-'),
           sg.FilesBrowse(file_types=(('Text and CSV', '*.txt;*.csv'), 
                                    ('CSV', '*.csv'),
                                    ('Text', '*.txt'),
                                    ('All', '*')))],
          [sg.Button('Read'), sg.Button('Exit')]]
```
!!! note "Code Snippet"
    If a code snippet would be useful to have, let me know! I'll happily provide a sanitized version of the code. The only things edited out would be calculations and specifications, as those are under NDA.

## End Result
The end result is a program that is faster and more consistent than manual data analysis. Program isntallation and updating is user friendly, as I have the program packaged into an installer (Inno3D). 

## Future Plans
I hope to expand my programming skill in the future by continuing to improve on Python, and refreshing myself with C++ and Java. I'll likely be re-writing the program in C++ for faster execution and better modularity for different departments. 

