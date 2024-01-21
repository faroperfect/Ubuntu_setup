### Step.1 recursively get the dependencies.  
<https://stackoverflow.com/questions/22008193/how-to-list-download-the-recursive-dependencies-of-a-debian-package>  
apt-cache depends --recurse --no-recommends --no-suggests --no-conflicts --no-breaks --no-replaces --no-enhances <your-package-here> | grep "^\w" | sort -u  
Be attention, this list contains "apt-offline" it self. remove its name if u want to use Step.2.  


### By the way, there is a problem when I try to download the files of Ubuntu in mirror site.  
`https://askubuntu.com/questions/1279002/what-is-the-difference-between-suite-and-suite-security-repositories-in-apt`  
according to this answer, the most convinent approach is use the only "focal" version. It is the basic version and have the full dependencies itself needs.   

### Step.2 download these .deb file and make a list   
`apt-get download <Step1 dependencies' name without itself's name>`  
use `apt-get` but not `sudo apt-get`.  

