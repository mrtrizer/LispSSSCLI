Main Page {#mainpage}
=========
# LispSSS
##Install LispSSS
To install:

	git clone https://github.com/mrtrizer/LispSSSCLI.git lispsss
	cd lispsss
	cmake -G "Unix Makefiles"
	make
	make install

##Hello, World!
Create file helloworld.sss and mark it executable. Than fill it next code:

	#!/usr/local/bin/lispsss
	print "Hello, World!"

Run script:

	./helloworld.sss

Or:

	lispsss helloworld.sss

# Documentation
See some diagrams in engine/doc.
