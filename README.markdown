check-vc.slax is a proof-of-concept poller for the internal PFE and VC
ports. It pushes the traffic stats as found: root@switch> show
virtual-chassis vc-port statistics into a bunch of rows. If the
interface names stay the same, the OIDs should do so as well. YMMV.

WARNING!! On a 3 member EX4200-24T stack, this takes almost 3 minutes to
run, and drives the load up to 1.75! I found that on a 2 member
EX4200-24T stack, it only takes 1 minute, so the load is less
noticeable. I imagine that a highly loaded switch might fall over.

install this script in fpc0:/var/db/scripts/op/check-vc.slax
even though it is an event script.
