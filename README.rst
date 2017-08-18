*******************************************************************
pyGmt: A simple python wrapper for the Generic Mapping Tools (GMT).
*******************************************************************

Writen by Weijia Sun.


The tutorial can be found at `pyGmt <http://pygmt.readthedocs.io/>`_.


Examples
--------

To plot Great Britain, Italy, and France in blue with a red outline and Spain, Portugal and Greece in yellow (no outline), and pick up the plot domain form the extents of these countries, use

>>> import pyGmt
>>> gmt = pyGmt.Gmt()
>>> gmt.comment("plot a coastline")
>>> gmt.cmd("pscoast", "-JM6i -P -Baf -EGB,IT,FR+gblue+p0.25p,red+r -EES,PT,GR+gyellow > map.ps")

or

>>> gmt.shell("gmt pscoast -JM6i -P -Baf -EGB,IT,FR+gblue+p0.25p,red+r -EES,PT,GR+gyellow > map.ps")

and now you would see a 'rungmt.sh' in the current directory. Then use

>>> gmt.execute()

to run the script.

Installation
------------

Downloat the code and run
>>> python setup.py install
