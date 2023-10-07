# Linux-basic-commands-assignment

## Create a user with user group
sudo adduser devops
sudo usermod -aG devops devops

## switch user
su devops

## Create two directories in user's home directory named os-concepts and ubuntu-is-the-best
mkdir os-concepts ubuntu-is-the-best

## Create two files on each directory
cd os-concepts/
touch os-concepts.txt
cd ../ubuntu-is-the-best/
touch ubuntu-is-the-best.txt

## List the files with detailed information ( including file permission )
ls -l

## Update file permission so that owner can read,write and group can only read and others can not do anything
chmod 640 os-concepts.txt 
cd ../ubuntu-is-the-best/
chmod 640 ubuntu-is-the-best.txt

## Create another group
sudo addgroup devops-2

## Update file ownership to the newly created group
cd ..
sudo chown -R: devops-2 os-concepts/
sudo chown -R: devops-2 ubuntu-is-the-best/

## Add the user to the new group




