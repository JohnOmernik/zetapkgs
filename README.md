# zetapkgs
Reviewed Packages for Zeta Architecture
-----------
# Package Standards
As part of zetapkgs, standards will be created and proposed in this package. The goal is to help with the upkeep, patching etc of packages installed in Zeta. 

## Legacy Migration
------------
Previous packages for Zeta were written by a lazy monkey with one arm tied behind his back. As such, consistency is suspect. There were two primary locations for packages. 


https://github.com/johnomernik/zetago

(And then under that in the pkgs directory)

and 

https://github.com/johnomernik/zetaextra

The idea was that packages in zetago were the approved packages, and zetaextra was a working space. 

Well, after careful review we are moving all packages out of zetago, and reviewed packages will exist in zetapkgs. 

As we come up with our standards in zetapkgs, we will move packages from zetaextra to zetapkgs, thus all packages found in ./pkgs in zetago will be moved to zetaextra. 

After doing a git pull on zetago, you may notive packages missing, and panic. Not to fret.  Follow these steps

1. Find a place for zetapkgs and clone this repo in the parent. 
2. If you don't already have a place for zeta extra, find a place for it and clone zetaextra in the parent
3. Update your conf file in zetago/conf/package.conf
   1. Change your CORE_PKG_LOC from ./pkgs to be location relative to ./zetago 
        - Example if ./zetago is /home/zetaadm/zetago and zetapks is /home/zetaadm/zetapkgs then change CORE_PKG_LOC to be "../zetapkgs"
   2. Ensure your ADD_PKG_LOC points to zetaextra and you should be solid 


 
