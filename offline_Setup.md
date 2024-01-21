### Obviously, a offline  install method is nesessary.  
I choose apt-offline. According to <https://stackoverflow.com/questions/22008193/how-to-list-download-the-recursive-dependencies-of-a-debian-package> the highest score answer, use this command below to recursively get the dependencies of it.  
`apt-cache depends --recurse --no-recommends --no-suggests --no-conflicts --no-breaks --no-replaces --no-enhances <your-package-here> | grep "^\w" | sort -u`  
It needs so many dependencies below:  
` adduser
apt
apt-offline
cdebconf
debconf
dpkg
gcc-12-base
gpgv
install-info
less
libacl1
libapt-pkg6.0
libaudit-common
libaudit1
libbz2-1.0
libc6
libcap-ng0
libcap2
libcom-err2
libcrypt1
libdb5.3
libdebian-installer4
libexpat1
libffi8
libgcc-s1
libgcrypt20
libgdbm-compat4
libgdbm6
libgmp10
libgnutls30
libgpg-error0
libgssapi-krb5-2
libhogweed6
libidn2-0
libk5crypto3
libkeyutils1
libkrb5-3
libkrb5support0
liblz4-1
liblzma5
libmagic-mgc
libmagic1
libmpdec3
libncursesw6
libnettle8
libnewt0.52
libnsl2
libp11-kit0
libpam-modules
libpam-modules-bin
libpam0g
libpcre2-8-0
libperl5.34
libpython3-stdlib
libpython3.10-minimal
libpython3.10-stdlib
libreadline8
libseccomp2
libselinux1
libsemanage-common
libsemanage2
libsepol2
libslang2
libsqlite3-0
libssl3
libstdc++6
libsystemd0
libtasn1-6
libtextwrap1
libtinfo6
libtirpc-common
libtirpc3
libudev1
libunistring2
libuuid1
libxxhash0
libzstd1
mailcap
media-types
mime-support
passwd
perl
perl-base
perl-modules-5.34
python3
python3-magic
python3-minimal
python3.10
python3.10-minimal
readline-common
tar
ubuntu-keyring
zlib1g `  

### By the way, there is a problem when I try to download the files of Ubuntu in mirror site.  
`https://askubuntu.com/questions/1279002/what-is-the-difference-between-suite-and-suite-security-repositories-in-apt`  
according to this answer, the most convinent approach is use the only "focal" version. It is the basic version and have the full dependencies itself needs.  

