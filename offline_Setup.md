### Obviously, a offline  install method is nesessary.  
I choose apt-offline. According to <https://stackoverflow.com/questions/22008193/how-to-list-download-the-recursive-dependencies-of-a-debian-package> the highest score answer, use this command below to recursively get the dependencies of it.  
`apt-cache depends --recurse --no-recommends --no-suggests --no-conflicts --no-breaks --no-replaces --no-enhances <your-package-here> | grep "^\w" | sort -u`  
