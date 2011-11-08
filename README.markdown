`check-vc.slax` is a proof-of-concept poller for the internal PFE and VC
ports. It pushes the traffic stats as found:

> root@switch> show virtual-chassis vc-port statistics

into a bunch of rows. If the interface names stay the same, the OIDs should
do so as well. YMMV.

This script may drive your CPU and load up during the polling - especially
if you have a lot of VC ports. I'm yet to make the polling smarter.

Install this script in `fpc0:/var/db/scripts/op/check-vc.slax`
even though it is an event script (?)
