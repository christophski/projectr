This app is for running projectors using raspberry pis. Hook up the projector to the raspberry pi. Navigate to the pi's web address to upload images and select what is displayed on the projector.
This is a fairly old project using webpy, which I found to be a useful way to learn python because of it's barebones approach.

Run both projector.py and server.py on the raspberry pi

If no raspi available you can use
> python projector.py -t
To test in a window.

This is the version using TCP for communication.

Requirements
* pi3d
* python-yaml
* python-pickle
* python-webpy
* python-pil

UI
---

Desktop view:

![Desktop view](/docs/desktop.jpg?raw=true "Desktop View")

Mobile View:

![Mobile view](/docs/mobile.jpg?raw=true "Mobile View")


RASPBERY PI SET UP
----------

SET AUTOLOGIN


> # Check if logged in via SSH, if not run these
> if [ -z "$SSH_CLIENT" ] ; then
>     python projector.py &
>     python server.py &
> fi