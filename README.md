# eliark-iso
#
# Created by ELIAS WALKER 
# 
# These programs are free software; you can redistribute them and/or modify
# them under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
# 
# These programs are distributed in the hope that they will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston,
# MA 02110-1301, USA.

############################################################################


# EliArk is under development. so dont expect everything to work perfectly. 
# calamares is currently broken in this release. but should be fixed in the next. 
# I am aware of the issues with conky. it is fixed for the next release
# if you find any other bugs or have any suggestions you can contact me at 

# eliasw4u@gmail.com


############################################################################

# to install arch
# format the drive you want arch installed to. using cfdisk or the likes
# then mount it to /mnt (this is Very important. because the script assumes it is mounted there

mount /dev/sdx0 /mnt

# (x0) being the drive letter and partition number)
# like this,,,
               mount /dev/sda1 /mnt

# if you are not sure run
lsblk 



# then after that is finnished and everything is mounted correctly (and internet is working)

# run (as root) 

sudo ./strap-in

# then when that is finnished open install-me with nano

sudo nano install-me

# change line 33

echo "hostname" > /etc/hostname  

# change "hostname" to whatever you want. but keep the quots, like this

echo "eli" > /etc/hostname  

# then change line 37, 39, and 41

useradd -m -g users -G wheel,storage,power -s /bin/bash user  

# and

passwd user

# and

echo "user ALL=(ALL)" ALL >> /etc/sudoers

# replace "user" in ALL THREE lines with whatever username you want

# type ctrl-X then y then enter

# now enter

sudo ./install-me

# this will install the base system, add user, set permissions, and set it up to boot the new arch 

# then you can use my arch1 script to install a desktop and many other things. 

# in this one you also need to change the username in line 173 or in option #6 to what you want

sudo nano arch1

     adduser username wheel ;;
     
# change username to what you want (you may also want to change it in line 122
# but line 122 is just cosmetic and will still work without a change)

# ctrl-X then y then enter

# then run (as root)

sudo ./arch1

# then just go down the list a,b,c,d,e,f
# and install what you need or want.
# if you miss something you can alway run arch1 again. 

