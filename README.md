# easymill
A bash file to automate FlatCAM to produce a single gcode file for milling PCBs with a fixed end mill bit.

A simple bash script which can be customized to generate single sided PCBs from gerber and drill files. Modify to suite your needs. Specifically you will want to set the path to FlatCAM and the end mill diameter size.

## Requirements
This script requires that the gerber file names indicate what they are for and contain the strings "Edge_Cuts" or "B_Cu"/"F_Cu". This is the same that KiCAD produces. Also I recommend combining drill files. Finally, you will want to make sure the origin of your PCB has been defined if using KiCAD and that the files are exported with "Use auxillary axis" checked.

For single sided milling only. If you use B_Cu and an Edge_Cuts file then the copper layer will be mirrored so that your through hole components will mount on the back. If you don't want this you can use the F_Cu layer for your copper traces in which case no mirroring will occur.

## Usage

The script takes no parameters, but has many different settings which can be customized to fit your processes. These are changed by editing the script file. To run the script is as simple as:

```
cd /directory/with/gerber/files/
/path/to/easymill
```
