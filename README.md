# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting
```
DEVELOPED BY:SUSITHRA.B
REGISTER NO:212223220113
```
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
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/7c94ebc1-b1f4-46e7-8353-417142fd38c8)

cat < file2
## OUTPUT
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/501cf5f0-1fbc-42b6-bfe7-9b57e73f90b3)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/6a4feb72-c671-4825-85aa-c6376aabc865)

comm file1 file2
 ## OUTPUT
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/cdd9477a-2786-4100-b20f-6d7796c5ca32)

 
diff file1 file2
## OUTPUT
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/1bc74ff8-1720-41bb-9cc8-6fc455efbd18)


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
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/3dc744ec-c1a8-44a2-9989-58569c7427a1)


cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/e249ccc9-52cb-459a-8b04-1ba75d3b2dcb)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/38d538d5-5ad7-4d12-ad0d-a111c606ac1a)



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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/e20e39be-7e0f-43dd-b6f6-34fa5acf1ee0)


grep hello newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/9ec8f876-3c82-4240-8c4e-1df38517a4b6)





grep -v hello newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/ea699bd8-5825-43b4-8709-910ac885c03f)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/e63d3d49-866b-4fbe-bc6d-73b76420d052)





cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/6610b324-6c85-4287-9584-846b02f350dc)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/5978c886-91da-4a7d-a192-0abf8565a264)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/c50ca298-07f5-443f-bcbc-4b954e4aa0a7)



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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/91f65fcf-ae1c-4af7-ba01-9e08dae4344f)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/478bbcdb-0059-4438-9d7f-7a58681af193)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/22831997-ba0b-4287-95bb-a624e91ef667)




egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/ee500936-af91-4b89-aded-c137ad85c752)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/5107010e-2b77-4efc-b8e1-1faacf061e4e)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/0df5b1af-62d3-4500-9423-bd1482190594)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/d9c58e34-386a-4f41-8e1c-4cb5d5eb6126)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/bdaa5946-4c3a-4756-94de-aa6de3e00f44)

egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/36af309b-5b03-4319-a88a-281463e33c08)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/2376391b-58ba-4273-b8b5-62c22d2deceb)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/6f2032e4-ba68-47be-a34d-603600df2740)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/a0f4d2f1-c486-4558-af29-69f54bd52f32)


cat > file22
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


sed -n -e '3p' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/b53f52bf-c87d-4192-8a31-69896f921e03)

sed -n -e '$p' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/2c38c861-d035-40c9-b1d2-0d36f299ee93)

sed  -e 's/Ram/Sita/' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/dab07896-47fc-47f1-8443-131597d01ee2)


sed  -e '2s/Ram/Sita/' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/337757d9-76f0-4eea-b0cb-a55729deb791)

sed  '/tom/s/5000/6000/' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/5b30908a-802c-47ca-a57f-37b5d5ffd22e)

sed -n -e '1,5p' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/dc5dfbb3-7742-4db8-be87-a20240569c0a)

sed -n -e '2,/Joe/p' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/b348705d-3fa2-4a18-80b3-c1b267ed9547)


sed -n -e '/tom/,/Joe/p' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/46fe07a8-7218-41b7-af9d-bb11fc2ed472)


seq 10 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/8e9d9608-5ce6-48d1-bedb-34350cd87121)




seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/824a8a6d-598b-4c62-8217-338ceefe70f2)

seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/c50bec67-3308-42a8-afed-a32963b717a1)




seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/3e57fe1c-ecc1-4e2f-8be8-c705433fc1bc)




seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/a744fe85-c479-4b9b-8af2-7e5852122514)



seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/575e3cfd-d5b5-4b9c-9dfd-9976ff43524c)



sed -n '2,4{s/^/$/;p}' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/a436aa71-2f79-4c09-a1af-7e4c74a1e500)



sed -n '2,4{s/$/*/;p}' file22
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/d5d99a04-6420-495f-bf5f-35efbd4c9be5)


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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/78194905-6341-47cc-bd27-c8f9e72cc7bb)



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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/a6d87eed-d403-4390-bdba-d2ccb18beed4)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/4b032cdd-d14d-4321-8174-3cce2e37a59e)

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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/88c1013e-6d4c-4032-9cce-1a5c2a43b69a)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/f99f0f21-e087-448a-9c45-36cabbff8fc5)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
```
bench.py
file1
file11
file2
file21
file22
file23
hello.c
hello.js
newfile
readme.txt
urllist.txt
```

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
```
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt
drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/
-rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt
-rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txt
```

tar -xvf backup.tar
## OUTPUT
```
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
```

gzip backup.tar

ls .gz
## OUTPUT
```
 backup.tar.gz
```
 
gunzip backup.tar.gz
## OUTPUT
```
backup.tar
```

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/5c190271-f1d4-48f3-89b1-16bcbd5dac2c)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/6343e586-5296-406b-aa48-30607347bc5e)


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
```
File name is ./scriptest.sh
File name is scriptest.sh
First arg. is 1
Second arg. is 2
Third arg. is 3
Fourth arg. is
The $@ is 1 2 3
The $\# is $#
The $$ is 124
```

 
ls file1
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/a6142d49-70e3-4262-8998-dee49678d7d7)


echo $?
## OUTPUT 

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/05ed26cc-aeca-4120-a01a-91ac63578697)

 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
1

 
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
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/b202be40-5ee6-4af1-81a9-1d863553840f)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
```
baseball is less than hockey
```



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
```
You are the owner of the /etc/passwd file
```

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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/0e848d5c-cc86-4fd3-9190-df56025c4845)


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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/003eb13e-b4a9-424d-9963-432bbce099ac)


# check if a file
cat > ifnested.sh 
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
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/a6ded381-a3d6-4d4d-bc54-a3a7b51e3eb1)


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
```
Welcome Ram
Please enjoy your visit
Welcome Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```

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

![image](https://github.com/SusithraB/OS-Linux-commands-Shell-script/assets/146347839/b834336c-349d-45bf-a492-d588346ec9e6)


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
```
Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```
 
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
 ```
 10
9
8
7
6
5
4
3
2
1
```
 
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
$ chmod 755 untiltest.sh
$ ./ untiltest.sh
 ## OUTPUT
 ```
 100
 75
 50
 25
```
 
 
 
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
$ ./forin1.sh
## OUTPUT
```
The next state is Alabama
The next state is Alaska
The next state is Arizona
The next state is Arkansas
The next state is California
The next state is Colorado
```
 
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
 
$ ./forin2.sh 
 
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
```
word:I
word:dont know if thisll
word:work
```
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ ./forin3.sh
## OUTPUT
```
word:I
word:don't
word:know
word:if
word:this'll
word:work
```


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
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
```
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam
```

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
```
The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
```

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
```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```
 
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
```
Iteration number: 1
Iteration number: 2
The for loop is completed
```
 
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
```
Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5
The for loop is completed
```
 
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
```
Enter your name: John
Hello John, welcome to my program.
```


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
```
Enter your name: sanju
Hello sanju, welcome to my program.
```



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

 ./funcex.sh  
 ./funcex.sh 1 2
 ## OUTPUT
 ```
$ bash script.sh 1 2
The result is 2
```

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
```
1
2
3
```
 
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
## OUTPUT
$ ./argshift.sh 1 2 3
```
1
2
3
```
 
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
## OUTPUT
```
+ (( 0 ))
+ set +x
```
 
 
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
```
total characters 75
Number of Lines are 10
No of Words count: 10
```
 
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
```
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome
```


# RESULT:
The Commands are executed successfully.
