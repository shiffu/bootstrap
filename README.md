# Ansible playbooks to configure from scratch a new Arch Linux installation.

They are 3 main playbooks to run to perform the entire Arch Linux installation from scratch:

+ The first one from the 'control' machine to prepare the target machine (partitions creation, disk formatting, etc...)
+ The second one from the 'target' machine once the arch-chroot as been performed to install base packages and prepare for the last playbook to run
+ The third and last playbook to finish up the installation including the desktop environment (could be either kde or i3)

Those playbooks expect a vault to be present (by default at: ~/.ansible/vaults/) with the following var defined:

+ root_pwd
+ ansible_user_name
+ ansible_user_group
+ ansible_user_pwd
+ ansible_user_salt
+ user_name
+ user_group
+ user_pwd
+ user_salt
+ local_user_name
+ local_user_pwd

I've built those playbooks to ease and speed up my Arch Linux installations but I would recommend anyone to actually go through the full installation manually to properly learn how their system is built from the ground up (check out the Arch Wiki).


> **Disclaimer**: These playbooks have been created by me for my personal use. You are free to use them too if you want but keep in mind that **they could wipe out your entire system** as some of them are creating partitions and formatting them. So use them at your own risk and with caution. They should be more considered as examples or informational material to help you building your own setup. You acknowledge, by your use of these playbooks, that your use of them is at your sole risk and that **I won't be responsible of any damage that might be caused to your own system**.
