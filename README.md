rsinit
======

rsinit is a minimalistic single binary init for the initramfs for embedded
systems. It's main objective is to mount the root filesystem as fast as possible
and then hand over to the actual init program.

The main use-case is, to mount root filesystems that cannot be mounted by the
Linux kernel directly. But it can also mount just about anything that the kernel
can mount directly based on the command-line.

Currently supported root filesystems are:

 * 9pfs with USB gadget transport
 * filesystems on a dm-verity device

 * regular devices or anything that requires just specifying the device and
   mount options
 * nfsroot
 * 9pfs with virtio transport (for QEMU)
