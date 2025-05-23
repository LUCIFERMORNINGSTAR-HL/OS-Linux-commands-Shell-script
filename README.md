# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![Screenshot 2025-04-23 095304](https://github.com/user-attachments/assets/a4872d03-7f45-4d67-91f4-a495bdd32f03)



cat < file2
## OUTPUT

![Screenshot 2025-04-23 100014](https://github.com/user-attachments/assets/38e4dd4f-4530-4d43-8190-d524d30c6b02)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![ex1 1](https://github.com/user-attachments/assets/65a878df-d9a6-4129-b20a-b63a3c3147db)

comm file1 file2
 ## OUTPUT

 ![ex1 2](https://github.com/user-attachments/assets/7791db23-c831-459f-a0f9-a81a01b9a662)

diff file1 file2
## OUTPUT

![ex1 3](https://github.com/user-attachments/assets/92532cdc-e65f-4b82-96f5-d9a29620ded0)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
cut -c1-3 file11
## OUTPUT

![ex1 3 1](https://github.com/user-attachments/assets/960507d2-fa50-4e64-ab85-fc2d85194d22)


cut -d "|" -f 1 file22
## OUTPUT

![ex1 3 2](https://github.com/user-attachments/assets/81b37390-78b8-4f58-b4aa-76ecb398652a)


cut -d "|" -f 2 file22
## OUTPUT
![ex1 3 3](https://github.com/user-attachments/assets/ef7dc6d2-d68b-4754-b4b9-48df8f36b216)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![ex1 4 1](https://github.com/user-attachments/assets/2d6fc7d1-86c0-40df-962a-8fe80f5285f0)



grep hello newfile 
## OUTPUT

![ex1 4 2](https://github.com/user-attachments/assets/e417c963-24a3-4f24-9f21-14b4b92ec335)


grep -v hello newfile 
## OUTPUT

![ex1 4 3](https://github.com/user-attachments/assets/ab28481b-4915-48cf-a38b-2855c261057c)

cat newfile | grep -i "hello"
## OUTPUT

![ex1 4 4](https://github.com/user-attachments/assets/e6909fdf-7f35-4e6f-aea2-4f6b83cdd595)


cat newfile | grep -i -c "hello"
## OUTPUT

![ex1 4 5](https://github.com/user-attachments/assets/fe1503bf-95eb-401d-9da2-d95fcfc374dc)



grep -R ubuntu /etc
## OUTPUT

![ex1 4 6](https://github.com/user-attachments/assets/d026b646-b402-4921-9b60-30d9c2e695c0)


grep -w -n world newfile   
## OUTPUT
![ex1 4 7](https://github.com/user-attachments/assets/a923db84-67b0-4300-a8fe-1fa0c848e2ee)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![ex1 5 1](https://github.com/user-attachments/assets/1114d735-eac0-4f3e-8b23-ef9ee4b8f94f)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![ex1 5 2](https://github.com/user-attachments/assets/864c165e-9de7-4b1b-8176-ad6402b09a72)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![ex1 5 3](https://github.com/user-attachments/assets/b93bff07-637d-4ecd-b7de-5133276cbb8a)



egrep '(^hello)' newfile 
## OUTPUT
![ex1 5 4](https://github.com/user-attachments/assets/9874d01e-20fe-4bc4-aa5c-b4926512cac8)



egrep '(world$)' newfile 
## OUTPUT

![ex1 5 5](https://github.com/user-attachments/assets/b3a6ab38-0bb9-499b-a432-2c48ff39c4d3)


egrep '(World$)' newfile 
## OUTPUT
![ex1 5 6](https://github.com/user-attachments/assets/ab859c9d-8a81-4f83-af37-d390ed8f0827)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![ex1 5 7](https://github.com/user-attachments/assets/9a6769f0-16a4-4be5-950f-87b178c956ec)


egrep '[1-9]' newfile 
## OUTPUT

![ex1 5 8](https://github.com/user-attachments/assets/b066ba5f-0242-4c6e-a3d7-e88834ee1f3e)


egrep 'Linux.*world' newfile 
## OUTPUT

![ex1 5 9](https://github.com/user-attachments/assets/49a59ef0-49da-4554-aa73-9e0ae320af8b)

egrep 'Linux.*World' newfile 
## OUTPUT
![ex1 5 10](https://github.com/user-attachments/assets/ef2615c9-47e8-41a2-b19f-e4102a6c9d77)


egrep l{2} newfile
## OUTPUT
![ex1 5 11](https://github.com/user-attachments/assets/aec6cce5-cc42-47f5-ba46-3e7e5d342875)



egrep 's{1,2}' newfile
## OUTPUT 
![ex1 5 12](https://github.com/user-attachments/assets/c0eea27d-18f1-479a-bce0-43791c5c29ec)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![ex1 6 1](https://github.com/user-attachments/assets/913b10b3-d165-4f03-8683-881fca7f99e2)



sed -n -e '$p' file23
## OUTPUT

![ex1 6 2](https://github.com/user-attachments/assets/1a579c2f-c728-450b-b3cb-0b675f83f603)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![ex1 6 3](https://github.com/user-attachments/assets/bac080da-d098-4d4a-81fc-3ae96ae630cf)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![ex1 6 4](https://github.com/user-attachments/assets/2d425319-f270-4c1c-b421-6231301b9a05)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2025-04-23 181504](https://github.com/user-attachments/assets/40142be9-f000-4a89-b82c-e41eb962bc06)


sed -n -e '1,5p' file23
## OUTPUT

![ex1 6 5](https://github.com/user-attachments/assets/ff5c4e51-1250-4120-ad34-825fc1dd884e)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![ex1 6 6](https://github.com/user-attachments/assets/1a12cd7b-ec84-44db-b088-0e1c3d2cb711)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![ex1 6 7](https://github.com/user-attachments/assets/e906f124-b729-4429-be7b-751c7d30f905)


seq 10 
## OUTPUT

![ex1 6 8](https://github.com/user-attachments/assets/d6191689-5fae-4ad5-a113-dbca846251a7)


seq 10 | sed -n '4,6p'
## OUTPUT

![ex1 6 9](https://github.com/user-attachments/assets/0dcc64d7-1391-4b8b-ae08-023b71d24e26)


seq 10 | sed -n '2,~4p'
## OUTPUT

![ex1 6 10](https://github.com/user-attachments/assets/6be13672-9015-4d0f-900b-280b80055ab7)


seq 3 | sed '2a hello'
## OUTPUT

![ex1 6 11](https://github.com/user-attachments/assets/33439a30-c1a2-4bd9-9dac-b33919b2b85a)


seq 2 | sed '2i hello'
## OUTPUT

![ex1 6 12](https://github.com/user-attachments/assets/60c6e493-0755-4dab-9fb6-39d305d5e021)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-04-23 195439](https://github.com/user-attachments/assets/04fd9802-450d-44c0-a722-2e56583bb3d8)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![ex1 6 13](https://github.com/user-attachments/assets/0ae203d9-f13d-45ac-855a-850a96be6d86)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot 2025-04-23 195635](https://github.com/user-attachments/assets/fd4049f0-bb35-4519-aa84-cce8d07c3edb)

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

![ex1 7 1](https://github.com/user-attachments/assets/bb7aa171-7a7f-41a3-b9df-73a343f15d56)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![ex1 12 1](https://github.com/user-attachments/assets/11e7743e-4768-4575-8b78-398a32cad82e)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![ex1 13 1](https://github.com/user-attachments/assets/595798d8-32eb-4458-9989-87b16bfd57a7)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

 ![ex1 14 1](https://github.com/user-attachments/assets/15f765e2-044a-4b36-ab07-8e9a4cf845f9)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![ex1 14 2](https://github.com/user-attachments/assets/1137238f-8250-42ef-bce5-667d736c3b18)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

![ex1 15 1](https://github.com/user-attachments/assets/8c3d171e-1794-4a78-97d7-be3820bf0b34)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![ex1 15 2](https://github.com/user-attachments/assets/b6a7498c-6b3f-49b2-9563-9ab85d69f189)

tar -xvf backup.tar
## OUTPUT
![ex1 15 3](https://github.com/user-attachments/assets/69487247-9cf4-4ead-b3db-88650de91edb)

gzip backup.tar
ls .gz
## OUTPUT
 ![Screenshot 2025-04-23 202614](https://github.com/user-attachments/assets/7fe0d60c-522d-4381-9cfc-65b1354a6a1a)

gunzip backup.tar.gz
## OUTPUT

![Screenshot 2025-04-23 202843](https://github.com/user-attachments/assets/1b9f9712-f986-4016-9c05-05f0a88ddc30)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![ex1 16 1](https://github.com/user-attachments/assets/6b5fe8e0-3cf8-4c79-8432-1d90e80a6a5c)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![ex1 16 2](https://github.com/user-attachments/assets/db62ad35-1619-4226-a449-905781fdbfea)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 ![ex1 16 3](https://github.com/user-attachments/assets/eae0f3b4-9a26-40a2-a781-55935ceda7de)

ls file1
## OUTPUT
![ex1 16 4](https://github.com/user-attachments/assets/17dc9e8c-fd08-474e-b583-5fcfa87d25fe)

echo $?
## OUTPUT 
![ex1 16 5](https://github.com/user-attachments/assets/be813627-9144-43a0-80d2-efb2d1eadf21)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![ex1 16 6](https://github.com/user-attachments/assets/717f38fd-12ea-4ac8-bd1b-c14942fcf72b)
 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![ex1 17 1](https://github.com/user-attachments/assets/64d974c9-054f-424d-9dfb-b2d9cfc8593a)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![ex1 17 2](https://github.com/user-attachments/assets/8d6616b2-9914-4da6-bbdd-1d7a34899d15)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![ex1 17 3](https://github.com/user-attachments/assets/b31a958b-62c0-449b-9097-ba386fb683aa)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![ex1 17 4](https://github.com/user-attachments/assets/1b2c18cc-cb91-4828-80da-d879c8ba2831)


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

![ex1 17 5](https://github.com/user-attachments/assets/71e5d246-a929-41e6-915f-813086f07c99)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh
## OUTPUT
![ex1 17 6](https://github.com/user-attachments/assets/0d5c8808-8d89-4a55-8c0f-a92fcf9ce7ec)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

## OUTPUT

 ![ex1 17 7](https://github.com/user-attachments/assets/213fd9e9-6cdd-4ac7-bcde-fbfc31c37483)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

## OUTPUT

![ex1 17 9](https://github.com/user-attachments/assets/1bae7766-2ae3-4609-b9dc-c949da0caaed)

cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh



cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh

## OUTPUT

![ex1 17 12](https://github.com/user-attachments/assets/71026111-6d66-4349-9a5e-84bebd615316)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
## OUTPUT

![ex1 17 10](https://github.com/user-attachments/assets/e2da8264-72e6-4c49-87fb-af4ecc76e66b)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
 ## OUTPUT

 ![ex1 17 11](https://github.com/user-attachments/assets/0e6b608f-f8fb-4625-86b9-f8b5d3cd2b6c)


cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```

## OUTPUT

![ex1 17 13](https://github.com/user-attachments/assets/df89bcd3-5f24-4ac4-bcc4-2b9d43dd8c1b)

cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

![ex1 17 14](https://github.com/user-attachments/assets/d21af652-4c61-47a5-8203-fb388efab611)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

![ex1 17 15](https://github.com/user-attachments/assets/24ac88d8-dbaa-44a4-931d-f26d3eb0b43e)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 ![ex1 17 16](https://github.com/user-attachments/assets/40895a96-daf9-442f-99d7-6c06c44cec64)

cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT

![Untitled design (1)](https://github.com/user-attachments/assets/35bc1c24-9e62-439a-8a06-9344e4c47dfb)

cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT

 ![Untitled design (2)](https://github.com/user-attachments/assets/a1a7dd49-7b54-4c59-a19b-393385a845c7)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

![Screenshot 2025-04-23 233459](https://github.com/user-attachments/assets/cc870de4-b230-453d-be58-6ea819b64cfe)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2025-04-23 233459](https://github.com/user-attachments/assets/d0cecd06-8c73-4bab-95a6-9e162087d494)

$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
./funcex.sh 1 2

 ![Screenshot 2025-04-24 003557](https://github.com/user-attachments/assets/c58e8770-4569-41f0-8088-007b0f99852d)

cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT

 ![Screenshot 2025-04-24 003905](https://github.com/user-attachments/assets/f3d868dc-3140-4080-9a82-1525fd485d82)

 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT

 ![Untitled design (3)](https://github.com/user-attachments/assets/7e3f8b08-e20e-4cbc-adab-36ed7569cb90)

cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
./argshift.sh 1 2 3
## OUTPUT
 
 <img width="323" alt="Untitled design (4)" src="https://github.com/user-attachments/assets/e11386bd-385c-4294-8404-7748ad63a451" />

cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![Untitled design (5)](https://github.com/user-attachments/assets/929d778c-f44e-4efc-b9b6-0461cb389359)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 

![Untitled design (6)](https://github.com/user-attachments/assets/6381cc60-5efb-4831-b563-5407bb7df520)

# RESULT:
The Commands are executed successfully.
