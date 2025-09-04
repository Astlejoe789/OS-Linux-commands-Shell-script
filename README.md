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

<img width="272" height="161" alt="image" src="https://github.com/user-attachments/assets/f379108e-a2d6-4859-b74f-907f3d6e7a78" />


<img width="368" height="130" alt="image" src="https://github.com/user-attachments/assets/4f7980a8-d35a-45ef-905c-8c3d2f008595" />

cat < file2

## OUTPUT

<img width="283" height="236" alt="image" src="https://github.com/user-attachments/assets/a0a84f80-c994-4ea2-8720-09b594f3a84f" />


# Comparing Files
cmp file1 file2

## OUTPUT
 <img width="368" height="130" alt="image" src="https://github.com/user-attachments/assets/4f7980a8-d35a-45ef-905c-8c3d2f008595" />
comm file1 file2
 ## OUTPUT
<img width="548" height="416" alt="image" src="https://github.com/user-attachments/assets/c80d7bba-94de-4045-86f4-9a32aaa62fdd" />

 
diff file1 file2
## OUTPUT

<img width="512" height="350" alt="image" src="https://github.com/user-attachments/assets/aaeff9fa-fa7f-4895-ba82-6b315a7edf2c" />

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

<img width="365" height="122" alt="image" src="https://github.com/user-attachments/assets/e0a89f3c-23bf-4239-b98b-c8e9454c7f55" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="487" height="186" alt="image" src="https://github.com/user-attachments/assets/2dc31fac-261c-497f-9a54-21e800a36a6c" />


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

<img width="521" height="152" alt="image" src="https://github.com/user-attachments/assets/2f8d69b5-d280-4147-98e0-4a2767f7a6bb" />



grep -v hello newfile 
## OUTPUT

<img width="406" height="127" alt="image" src="https://github.com/user-attachments/assets/e3b9dade-4d00-4630-9516-642bd7bfa3f4" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="518" height="167" alt="image" src="https://github.com/user-attachments/assets/3fa6aa80-63f6-4570-a072-b0bb9082a075" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="407" height="106" alt="image" src="https://github.com/user-attachments/assets/fa71cc31-348b-46c9-9f46-35d4450bcca8" />


grep -R ubuntu /etc
## OUTPUT

<img width="1633" height="652" alt="image" src="https://github.com/user-attachments/assets/6d4df594-1417-4c66-b5dc-6e4fad7b4033" />


grep -w -n world newfile   
## OUTPUT

<img width="617" height="156" alt="image" src="https://github.com/user-attachments/assets/aa036c7c-05ab-4ca9-aa31-9258e74b539d" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
## OUTPUT

<img width="601" height="223" alt="image" src="https://github.com/user-attachments/assets/0277b866-29e9-4927-8d77-0edd08202d1b" />

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
<img width="545" height="170" alt="image" src="https://github.com/user-attachments/assets/ee021a2c-ab64-4430-be7a-217083a25ac7" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="465" height="156" alt="image" src="https://github.com/user-attachments/assets/5db0d708-0788-43a4-9c76-d9e9e3aa413a" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="518" height="170" alt="image" src="https://github.com/user-attachments/assets/cda83d7e-16ff-47f9-81ac-5926f7c72877" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="447" height="133" alt="image" src="https://github.com/user-attachments/assets/39ec6677-588c-455e-8bcb-aa9be4d537b6" />


egrep '(world$)' newfile 
## OUTPUT

<img width="428" height="147" alt="image" src="https://github.com/user-attachments/assets/3659498f-001c-4626-a226-8d29d6649e3a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="537" height="182" alt="image" src="https://github.com/user-attachments/assets/8643ef68-f0ca-450f-bc98-9061a0caa094" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="480" height="125" alt="image" src="https://github.com/user-attachments/assets/161116b7-3022-4c16-ad51-5639f4458e16" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="480" height="125" alt="image" src="https://github.com/user-attachments/assets/a5c1b546-485f-486d-ae88-d269b987c765" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="447" height="132" alt="image" src="https://github.com/user-attachments/assets/fd7c248a-ceaa-491d-97d6-5ef3672b6bc7" />

egrep l{2} newfile
## OUTPUT

<img width="383" height="176" alt="image" src="https://github.com/user-attachments/assets/52a1660b-70dc-4399-9f96-1da7ff5ae259" />


egrep 's{1,2}' newfile
## OUTPUT

<img width="468" height="180" alt="image" src="https://github.com/user-attachments/assets/f4f945ce-7829-4bc1-9144-94eaea9a5a2b" />


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

<img width="460" height="336" alt="image" src="https://github.com/user-attachments/assets/08cb3513-e07d-4e27-b542-f2e4103f0661" />


sed -n -e '$p' file23
## OUTPUT

<img width="407" height="143" alt="image" src="https://github.com/user-attachments/assets/7fef791e-da77-4ae9-9775-3a92833666d5" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="731" height="336" alt="image" src="https://github.com/user-attachments/assets/fbbd64c1-82a6-4b35-9b1f-ba0abf0bf628" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="691" height="350" alt="image" src="https://github.com/user-attachments/assets/98d50593-1f79-41be-92eb-15debfcd9db8" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="578" height="273" alt="image" src="https://github.com/user-attachments/assets/109e3653-00ed-4041-8caa-b05f4b6bf83e" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="452" height="251" alt="image" src="https://github.com/user-attachments/assets/4485e517-78d8-42de-ad97-2d96ca719ced" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="423" height="181" alt="image" src="https://github.com/user-attachments/assets/1f368542-3db0-4ee3-8081-4f8f180748ed" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="472" height="151" alt="image" src="https://github.com/user-attachments/assets/51a0d97b-d4ac-4ac9-b061-10070e6834f1" />


seq 10 
## OUTPUT

<img width="498" height="362" alt="image" src="https://github.com/user-attachments/assets/177800da-b402-46e7-93fb-191309b5d5fa" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="472" height="180" alt="image" src="https://github.com/user-attachments/assets/f0a5dbb2-96cb-400a-ae0b-b1723f24b386" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="417" height="185" alt="image" src="https://github.com/user-attachments/assets/2685e0cc-d4c5-4815-8644-29de91721f08" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="467" height="157" alt="image" src="https://github.com/user-attachments/assets/f0f3c9c7-5ad4-4fd7-a3aa-f4bb636b3fa5" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="417" height="180" alt="image" src="https://github.com/user-attachments/assets/80877897-1765-4ce0-bb18-38a426ec3fa5" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="517" height="200" alt="image" src="https://github.com/user-attachments/assets/f83e8f6b-0a9b-4056-a68e-258baafb34dd" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="566" height="185" alt="image" src="https://github.com/user-attachments/assets/5140aaae-22c2-46f1-9f2b-1da156e8bba7" />


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT

<img width="471" height="177" alt="image" src="https://github.com/user-attachments/assets/5ee070a7-0bc4-4785-bb18-b723388d8e3c" />


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

<img width="1052" height="387" alt="image" src="https://github.com/user-attachments/assets/b6a26be7-0809-4089-8120-8a2373830058" />


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

<img width="672" height="248" alt="image" src="https://github.com/user-attachments/assets/051aee28-cfe7-437a-b05b-397a7a1f9c3d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="788" height="336" alt="image" src="https://github.com/user-attachments/assets/a3563025-9ed3-4e06-9bc2-4f28a3db799b" />

 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
```
## OUTPUT

<img width="537" height="205" alt="image" src="https://github.com/user-attachments/assets/05f7634c-d972-49a9-8d19-e74920a71751" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="613" height="262" alt="image" src="https://github.com/user-attachments/assets/9ab48e44-f528-439e-9c33-6599e615acff" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="586" height="307" alt="image" src="https://github.com/user-attachments/assets/9e2f419a-6901-4b30-9237-0a74cc6bc7ed" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="767" height="297" alt="image" src="https://github.com/user-attachments/assets/97ec0d10-6b5a-44b4-b477-43787e9f2390" />

tar -xvf backup.tar
## OUTPUT

<img width="740" height="291" alt="image" src="https://github.com/user-attachments/assets/2914199a-b7dd-4a87-bb87-de1bb749a70d" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="542" height="127" alt="image" src="https://github.com/user-attachments/assets/1e6b440b-9bce-40b7-82e2-6c682c8f05e7" />

gunzip backup.tar.gz
## OUTPUT

<img width="488" height="312" alt="image" src="https://github.com/user-attachments/assets/423babd9-7da1-48d7-b445-87183d9b3462" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="567" height="200" alt="image" src="https://github.com/user-attachments/assets/e5d800a4-472e-4ed2-8911-de753d6cd396" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="815" height="487" alt="image" src="https://github.com/user-attachments/assets/8a76df9b-a4e3-48da-bba0-f4f812a36c47" />


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

<img width="750" height="500" alt="image" src="https://github.com/user-attachments/assets/55ab80d6-53e6-4cd2-b2cc-675fdb06312d" />
 
ls file1
## OUTPUT

<img width="927" height="138" alt="image" src="https://github.com/user-attachments/assets/4a8b00c6-8ca3-4ffb-a83c-f6df946e2c89" />

echo $?
## OUTPUT 

<img width="562" height="146" alt="image" src="https://github.com/user-attachments/assets/6c459c5d-defc-4062-a728-886b5185d6e9" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="637" height="287" alt="image" src="https://github.com/user-attachments/assets/a9f6589e-5ed5-4784-9a7b-699e01a44d77" />

abcd
 
echo $?
 ## OUTPUT

<img width="637" height="287" alt="image" src="https://github.com/user-attachments/assets/8bb16910-2f80-4cd2-9197-ac4f0e8b5088" />

 
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


## OUTPUT

<img width="962" height="381" alt="image" src="https://github.com/user-attachments/assets/47466c7e-08e6-4011-81af-e783ff6edcdb" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="685" height="182" alt="image" src="https://github.com/user-attachments/assets/73a804d8-7d9a-4d9d-890e-c0ebbeaf04fb" />


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

<img width="587" height="148" alt="image" src="https://github.com/user-attachments/assets/46a5597a-2f9d-40b4-9bc4-4affd95bf96f" />

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

<img width="671" height="288" alt="image" src="https://github.com/user-attachments/assets/e5193311-4e5a-4855-97ad-d54c55f99634" />



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



## OUTPUT

<img width="705" height="190" alt="image" src="https://github.com/user-attachments/assets/f1694ce3-8c25-4bcb-b3f2-6a5b01dfb5fb" />

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

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
```

## OUTPUT

<img width="507" height="201" alt="image" src="https://github.com/user-attachments/assets/d9f4ef5c-4c26-4d27-ad55-f495288b433d" />


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

<img width="535" height="162" alt="image" src="https://github.com/user-attachments/assets/54194aeb-8fa7-4a90-ab11-1a0ee8598737" />

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

<img width="503" height="150" alt="image" src="https://github.com/user-attachments/assets/025e5767-9c5f-4ba6-85cd-9ef4757f9da6" />

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

 <img width="448" height="142" alt="image" src="https://github.com/user-attachments/assets/544389ae-fe8e-49f0-844c-fa241da6dd7d" />

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

 <img width="412" height="402" alt="image" src="https://github.com/user-attachments/assets/f78670bb-90bb-4017-beda-3347cc66099f" />

  
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
 
 <img width="565" height="350" alt="image" src="https://github.com/user-attachments/assets/2344291e-0e49-49c2-9844-ff8903b90ba1" />

 
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
<img width="502" height="345" alt="image" src="https://github.com/user-attachments/assets/49dd1db3-9452-4e34-a726-ff62b07afaf0" />

 
 
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

<img width="585" height="282" alt="image" src="https://github.com/user-attachments/assets/8e8116dc-be0a-4a60-b887-413c19fec24f" />

# cat cities

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

<img width="436" height="337" alt="image" src="https://github.com/user-attachments/assets/12ee8173-3c7c-452e-8d7e-445a4a3697d1" />




## cat forctype.sh 

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

<img width="512" height="278" alt="image" src="https://github.com/user-attachments/assets/5def622c-68ee-4cb5-bc7c-98e3caf3bdf9" />


## cat forctype1.sh 
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

<img width="452" height="250" alt="image" src="https://github.com/user-attachments/assets/6986a8c8-ccae-4b41-930c-13600fc7d90c" />


## cat fornested1.sh 
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

<img width="453" height="296" alt="image" src="https://github.com/user-attachments/assets/90edd21c-5a08-4623-b90a-91b27a8709b3" />

 
# cat forbreak.sh 
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

<img width="632" height="417" alt="image" src="https://github.com/user-attachments/assets/81293f48-9f91-4e63-a721-0610059fb09f" />

 
# cat forbreak.sh 
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

<img width="455" height="227" alt="image" src="https://github.com/user-attachments/assets/f4940e58-0d41-4e43-abbf-08e543814506" />

 
# cat exread.sh 

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

<img width="472" height="217" alt="image" src="https://github.com/user-attachments/assets/38691664-eb13-49ee-9516-d114614314db" />


# cat exread1.sh

```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT

<img width="525" height="237" alt="image" src="https://github.com/user-attachments/assets/6f3c8cec-443d-4238-8170-7623071310f8" />

 
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

<img width="391" height="187" alt="image" src="https://github.com/user-attachments/assets/301f2fe1-5a9b-4137-931c-3aa5a4c8ebd4" />
 
# cat argshift.sh
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

<img width="368" height="167" alt="image" src="https://github.com/user-attachments/assets/61457cd7-54c1-4178-88f9-cb7058e3797a" />

 
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

 <img width="367" height="210" alt="image" src="https://github.com/user-attachments/assets/00d4b690-4b75-42cd-b1a9-fcfe6d92734b" />

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
 
 <img width="410" height="427" alt="image" src="https://github.com/user-attachments/assets/ab12255a-c3e7-4042-a0f9-2ff580094853" />

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

 <img width="397" height="412" alt="image" src="https://github.com/user-attachments/assets/e23eb0d7-2a6d-469d-aecc-61c67268e221" />

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

<img width="358" height="197" alt="image" src="https://github.com/user-attachments/assets/8e125e80-49fe-49e0-9202-aac9ef1fdf65" />


# RESULT:
The Commands are executed successfully.
