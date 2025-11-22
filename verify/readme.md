GerbMerge Verification
==========================

This is a simple way to verify the program.
It will not detect possible problems with other Gerber files
but it is better than nothing.

rm -f merged/*
python2 ../../gerbmerge/gerbmerge.py --place-file=Placement.txt layout.cfg

Check if the generated files differ.

There is an error in the original millimeter files. 

INCH,LZ seems to work 
but 
METRIC,LZ puts the holes in the wrong place in Gerbv.
METRIC,0000.00 makes everything correct.

This is fixed by hand in the
millimeters/merged_orig files.


