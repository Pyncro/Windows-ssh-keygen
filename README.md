# Windows-ssh-keygen

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"


Enter file in which to save the key (/home/youruser/.ssh/id_rsa): [press Enter or specify custom name]
Enter passphrase (empty for no passphrase): [OPTIONAL but recommended]



# Putty-ssh-keygen

https://www.youtube.com/watch?v=Gx4KYpKs1i8


#### WARNING

New-SSHSession doesn't recognize PuTTY's key format (unfortunately neither the Gallery nor the project page mention this, but I found it in a PowerShellMagazine article). You need the private key in the OpenSSH format. You can convert the private key with PuTTYgen:

Click File → Load private key.
Enter the passphrase if the key is password-protected.
Click Conversions → Export OpenSSH key.
Enter the filename for the exported key (do NOT overwrite the PPK file) and click Save.
Exit PuTTYgen.



## Ubuntu-config

nano /etc/ssh/sshd_config

#Include /etc/ssh/sshd_config.d/*.conf
PubkeyAuthentication yes
PasswordAuthentication no
PermitEmptyPasswords no
