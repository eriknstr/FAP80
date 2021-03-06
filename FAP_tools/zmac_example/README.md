# Programming FAP80 in assembly

This is a simple FAP80 program in Z80 assembly. It displays the FAP logo, then listens to keyboard and prints whatever you type on the screen.

I'm using zmac as the cross assembler. Download it [here on the top right](http://members.shaw.ca/gp2000/zmac.html), it seems to have a windows executable, and if you're on macOS or linux you'll have to build it from source, just typing `make` should be enough.

Anyway put the `zmac` executable in the [PATH for windows](http://www.howtogeek.com/118594/how-to-edit-your-system-path-for-easy-command-line-access/), /usr/local/bin for macOS and linux, so you can invoke it directly in the command line. And while you're at it grab [hex2bin](http://hex2bin.sourceforge.net) and put it there as well.

Then run the ass.py to assemble the .z80 files. Actually if you take a look inside the ass.py you'll see it's some hacked together bash commands anyway, so you can run them directly if you want. It assembles the .z80 file with zmac, then convert .hex file into .bin file.

zmac also generates a number of other useful output files in the [zout](./zout) folder, most of all the .bds file, which stands for binary debuggable source. It lists all the instructions along with their memory address and data, so you can follow along while single stepping to see where you are in the program.

Finally use load.py to upload the program into the FAP80. And press RUN/STOP to start executing at full speed.