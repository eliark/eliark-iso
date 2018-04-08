# eliark-iso# Created by ELIAS WALKER 
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


# EliArk is under development. so dont expect everthing to work perfectly. 
# if you find any bugs or have any suggestions you can contact me at 

# eliasw4u@gmail.com


############################################################################

# to install arch
# format the drive you want arch installed to. using cfdisk or the likes
# then mount it to /mnt (this is Very important. because the script assumes it is mountes there

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

# change line 32

echo "EliArk1" > /etc/hostname  

# change "EliArk" to whatever hostname you want. but keep the quots

# then change line 36

useradd -m -g users -G wheel,storage,power -s /bin/bash eli  

# replace "eli" at the end with whatever username you want

# type ctrl X then y then enter

# now enter

sudo ./install-me

# be sure to first change line 32 and 36 to the username name hand to the hostname you want

# this will install the base system and set it up to boot the new arch 

# then you can use my arch1 script to install a desktop and many other things. 

sudo ./arch1

# then just go down the list a,b,c,d,e,f
# and install what you need or want.
# if you miss something you can alway run arch1 again. 

