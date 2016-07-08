all:

prog-picotap.sh: prog-picotap.temp.sh
	cat prog-picotap.temp.sh | sed -e 's@--curdir--@$(CURDIR)@g' > prog-picotap.sh

prog-jlink.sh: prog-jlink.temp.sh
	cat prog-jlink.temp.sh | sed -e 's@--curdir--@$(CURDIR)@g' > prog-jlink.sh

prog-jtagkey.sh: prog-jtagkey.temp.sh
	cat prog-jtagkey.temp.sh | sed -e 's@--curdir--@$(CURDIR)@g' > prog-jtagkey.sh




picotap: prog-picotap.sh
	jtag prog-picotap.sh

jlink: prog-jlink.sh
	jtag prog-jlink.sh

jtagkey: prog-jtagkey.sh
	jtag prog-jtagkey.sh

