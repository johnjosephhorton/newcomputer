# Preliminaries 

Copy the /home directory---ideally uncompressed---on to a removable
harddrive. 

# Install Arch Linux 


Install pip

Get latexlog2html from git

    git clone git@github.com:johnjosephhorton/latexlog2html.git
    cd latexlog2html
    sudo python setup.py install  

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


# Networking Configuration 

Arch uses netctl to control networking.
I addtionally needed `dhclient` (installed via pacman). To learn the name of
my network device, I just needed to find the name of the ethernet network device, which is eno1. 
    
I then created a profile in /etc/netctl/ which I called archether.
The contents are:

    Description='A basic dhcp ethernet connection'
    Interface=eno1
    Connection=ethernet
    IP=dhcp
    DHCPClient=dhclient

I then ran

    sudo netctl enable archether
    sudo netctl start archether

To test the connection:

    sudo ping -c 3 www.google.com 
