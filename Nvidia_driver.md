When using the .run file downloaded from NVIDIA offical website, it will report an error that YOU SHOULD TURN OFF X SERVER or something like that.
As a solution, refer to https://forums.developer.nvidia.com/t/how-to-exit-the-x-server-to-install-the-nvidia-driver/222361
"GataJapa" he or she 's answer:
sudo apt-get install nvidia-driver-515
//515 could be any other version number
//you can use ' apt-cache search nvidia-driver ' to find out which version you want.

It goes to an error
ERROR: NVIDIA driver is not loaded

and I will try this solution from https://askubuntu.com/questions/1153023/error-nvidia-driver-is-not-loaded
After checking:

BIOS
prime-select nvidia
nvidia-driver-XXXX package installed
uname -r header packages installed
and it was not working.

So the driver wasn't compiled for my kernel version. So I just did a

$ dpkg-reconfigure nvidia-dkms-4XX
and rebooted.
