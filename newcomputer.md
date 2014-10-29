# Preliminaries 

Copy the /home directory---ideally uncompressed---on to a removable
harddrive. 

# Install Arch Linux 

# Reasonable disk partitions 

Partition the drive into two partiions: 

    /sda
    / - root 
    /home 

They should both be ext4 filesystem.  

# Transfer files 

Find the attached hard drive 
   
    fdisk -l 

Suppose is it is `sdaX`---Mount the device to `/mnt` 

	sudo mount /dev/sdX 
	
Copy over files as needed using cp  

# Configure xmonad (~/.xinitrc) 

# ssh keys 

Create a symlink 

# Install 

git 
julia 
r 
latex 
pdflatex
ssh 
emacs 

