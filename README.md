# grub-fix
A fix for Gigabyte motherboards running GNU grub, allows disabling iommu, for faster boots.

# HOW TO

1. edit /etc/default/grub

change the part after GRUB_CMDLINE_LINUX_DEFAULT="

to include iommu=soft before the "" ends.

should look like this:

GRUB_CMDLINE_LINUX_DEFAULT="foo=2 blah=3 random=5 example=1 iommu=soft"

run

sudo update-grub

or if you're root,

update-grub

# You can now disable IOMMU and your boot will be vastly faster
