vrnetlab / Juniper vSRX
=======================
This is the vrnetlab docker image for Juniper vSRX.

Building the docker image
-------------------------
Download vSRX from http://www.juniper.net/us/en/dm/free-vsrx-trial/
Put the .vmdk file in this directory and run `make` to produce a docker
image named `vr-vsrx`. The version tag of the image will be the same as the
JUNOS version, e.g. media-srxmr-vmdisk-15.1X49-D80.4-disk1.vmdk will produce an image called
vr-vsrx:15.1X49-D80.4.

Please note that you should always specify the version number of the docker
image when running your router. Docker defaults to using 'latest' 
Please note that you will always need to specify version when starting your
router as the "latest" tag is not added to any images since it has no meaning
in this context.

Tested with:
 * media-srxmr-vmdisk-15.1X49-D80.4-disk1.vmdk  MD5:accdaf3b176a2a8cb95c16db7677b542

Usage
-----
The container must be `--privileged` to start KVM.
```
docker run -d --privileged --name my-vmx-router vr-vsrx
```
It takes a couple of minutes for the virtual router to start and after this we
can login over SSH / NETCONF with the specified credentials (defaults to
vrnetlab / VR-netlab9).

If you want to look at the startup process you can specify `-i -t` to docker
run and you'll get an interactive terminal, do note that docker will terminate
as soon as you close it though. Use `-d` for long running routers.


System requirements
-------------------
CPU: 2 cores

RAM: 3072MB

Disk: 1.5GB

FUAQ - Frequently or Unfrequently Asked Questions
-------------------------------------------------
##### Q: Do you have a question?
A: Uhhhh
