# junos-vsrx-vmdisk-15.1X49-D20.2.qcow2
VERSION=$(shell echo $(IMAGE) | sed -e 's/^junos-vsrx-vmdisk-\([0-9][0-9]\.[0-9][A-Z][0-9]\+\(\.[0-9]\+\)\?\(-D[0-9]\+\)\)[^0-9].*$$/\1/')

-include ../makefile-sanity.include
-include ../makefile.include

usage:
	@echo "Usage: put the Juniper vSRX .qcow2 file in this directory and run:"
	@echo "  make"

no-image:
	@echo "ERROR: you have no .qcow2 files"
