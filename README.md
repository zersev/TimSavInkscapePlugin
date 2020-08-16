# TimSavInkscapePlugin
Inkscape plugin for TimSav foam cutter

## installation:
place the servo.inx and servo.py files under <inkscape instalation folder>/share/extensions

## Usage:
### To generate GCode with several Servo values:
Place the different line types in different layers, Give the layer any name but include
in the name a keyword in the format: An<angle> and the produced GCode will set the servo 
angle accordingly. (for example all lines in a layer with keycode An60, will set the servo 
value to 60 degrees)

### Skipping layers:
Layers marked with keyword AnSkip, will be skipped from gcode generation

### Printing selected layers only:
In the Gui - a new fieald added: Filter. If this fieald is not empty, then only the layers
containing the keywords in the filter will be printed. For example Tail|Wing will print
any layer that includes 'Tail' or 'Wing' in its name.

### Drawing with pen (instead of cutting)
An offset of the pen can be configured assuming it is not in the same spot as the needle (x-offset, y-offset). 
Any layer that contains the keyword "Pen" in it, will apply this offset to the generated g-code. The offset 
values can be entered under the "Fill area" tab.

### Filling areas when using drawing pen:
Added "Fill area" Tab. This will fill any closed shape with a line pattern. Useful if using
a pen to draw on the foam board and filled shapes are desired instead of just outlines.
