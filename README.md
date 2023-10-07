# Linux-basic-commands-assignment

## Create a user with user group
```
sudo adduser devops
sudo usermod -aG devops devops
```

## Create two directories in user's home directory named os-concepts and ubuntu-is-the-best
```
mkdir os-concepts ubuntu-is-the-best
```

## Create two files on each directory
```
cd os-concepts/
touch os-concepts.txt
cd ../ubuntu-is-the-best/
touch ubuntu-is-the-best.txt
```
## List the files with detailed information ( including file permission )
```
ls -l
```

## Update file permission so that owner can read,write and group can only read and others can not do anything
```
chmod 640 os-concepts.txt 
cd ../ubuntu-is-the-best/
chmod 640 ubuntu-is-the-best.txt
```

## Create another group
```
sudo addgroup developers
```

## Update file ownership to the newly created group
```
cd ..
sudo chown -R :developers os-concepts/
sudo chown -R :developers ubuntu-is-the-best/
```

## Add the user to the new group
```
sudo usermod -aG developers devops
```

## Create a file called crash.in ( File should contain the word crash in it ) in different directories and then find the file in all the locations using find command
```
echo "crash in it" >> crash.in
cd os-concepts/
echo "crash in it" >> crash.in
cd ../ubuntu-is-the-best/
echo "crash in it" >> crash.in
cd ..
find /home/rafid -type f -name "crash.in"
```

## Then, replace the lines with crash to broken to all files ( use sed, xargs )
```
find /home/rafid -type f -name "crash.in" -exec sed -i 's/crash/broken/g' {} +
```







