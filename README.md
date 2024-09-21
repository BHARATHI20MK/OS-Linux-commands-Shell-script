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
![image](https://github.com/user-attachments/assets/d9e05616-1cb3-42e9-b453-9ee0c89a5a8c)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/5ffbe0a0-85a9-4fb6-97cb-fed7a2c6b320)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/9ad713f2-49ce-4a85-b9ba-99b5da29ae7f)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/b45facb0-23a9-463e-a6d0-9e9972409379)

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/b87bb893-1b24-4d3d-b649-2f10e412011d)

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
![image](https://github.com/user-attachments/assets/0599b333-611e-4006-b974-ef2df8d9d124)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/5d2be8b3-900e-446c-8737-f20c7be74683)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/37f01f30-32f6-40a5-9ae9-a0c9edb31d3c)

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
![image](https://github.com/user-attachments/assets/633be931-850e-4c63-9c7c-ee6e96256c88)
grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b7a19a25-a860-4335-9d4f-4d0abe1ebe04)
grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4be49f1b-ad88-4c7a-8f44-072fc74d0f67)
cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/9b3c3716-76aa-47b6-933c-f61218a23dd2)
cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/f8fd0748-5283-4c89-94d0-b33982e13746)
grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/a0e17e2c-51b0-4d49-9a9c-d0d74109a8eb)
grep -w -n world newfile   
## OUTPUT
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
![image](https://github.com/user-attachments/assets/3d565fbd-1646-42b0-b681-f7748d69eaf5)
egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/68edb1c9-c3cf-450a-9e55-05c956254952)
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/74d369b0-83b2-4aa6-9896-d5aa040784ea)
egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6de36527-c179-434c-8178-470b7fdd2820)
egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6cfce3f7-5c11-4a5a-885e-52f755da851c)
egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/90b18a0a-c360-432d-958e-7c60860b1fae)
egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/568306d0-72c2-449b-a555-37a7af624bcd)
egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8f328c9f-54e5-4166-8b9d-fd4efe680c6e)
egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d301be50-c464-42ef-8c7b-4e558083cfb9)
egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/15116670-5376-4d37-a5b0-80c24290c698)
egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/e74aa7e4-4f85-4d93-8f58-28ccf10b753d)
egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/8e4ca6cb-1184-4d42-8450-46e463025e55)
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
![image](https://github.com/user-attachments/assets/68ea760b-160a-462b-9ada-a4fa486ca24f)
sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/07745973-4a88-4c2b-85c3-efcf9e2d3ab4)
sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d46ae969-b95b-4bf9-b7d4-3bfaffd1f7af)
sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/8af4c756-7ab9-47bb-acd6-9c9d199c43a6)
sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/bc1ffcc9-31ac-4d4b-b1a3-19713baf9500)
sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/85241ea8-6387-4e8e-b432-6ac99878afc8)
sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b6667cf7-94f3-45c4-af03-46684aa386e3)
sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/c84dddcb-53f2-4c1a-94cb-9c22708bc320)
seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/f8c85ba4-f0f9-4926-ad1e-e4b3b54c7b2c)
seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/ffa7cc4d-a20a-45ce-8d52-c9c84c723680)
seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/f0e0b836-7307-46d8-96da-6eb90ab472c9)
seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/0367b5be-8fe6-41e2-b6f7-6ddcda56f8be)
seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/71999aab-069c-45bd-b371-1d47c58b0f81)
seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/7a343713-d34f-48ae-be0b-c63168c7211c)
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/70535ad6-a4dc-4691-b5a3-a28d74f814f1)
sed -n '2,4{s/$/*/;p}' file23


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
![image](https://github.com/user-attachments/assets/3c44c3e4-14bd-4136-9b0b-2c6fc9333416)
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
#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/4c4f2e62-5759-4b03-a178-065253650adc)
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
![image](https://github.com/user-attachments/assets/118e82fd-b94d-47d8-8d5a-fb30e91eb7c7) 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/5072f4ee-806b-4190-9509-c8f9b2a29ca4)
#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/8ee17339-457b-4b68-9e01-856be9715c3f)
mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/fee17506-8ee0-476b-9596-648196ca5287)
tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/0a9d7723-c0a3-4afd-8689-ee5166ba8820)
gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/7ddd7bd6-dab0-4258-a75b-b54cb6be000e)
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/2dcc9f33-9535-46bb-bc6f-f5e26492d8eb)
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/6a39e737-72f4-4b41-8579-4bfa4e7276ec)
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
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
ls file1
## OUTPUT
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied 
echo $?
## OUTPUT 
abcd
echo $?
## OUTPUT
![image](https://github.com/user-attachments/assets/e5bdd05c-4545-4a6c-9611-f6bab3835764)
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
##OUTPUT
![image](https://github.com/user-attachments/assets/36ad6352-6bd3-4125-9c32-ff06912b2ab1)
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/67bd107f-c0c0-4053-9bb6-6b1bb444ee34)
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
![image](https://github.com/user-attachments/assets/5b0e9880-e2be-4905-9191-58b629fb5d66)
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
![image](https://github.com/user-attachments/assets/044741fb-6ed1-4065-a2fe-425443299b2d)
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
##OUTPUT
![image](https://github.com/user-attachments/assets/311771a8-63ac-4951-ba0e-387800dcb602)
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
##OUTPUT
![image](https://github.com/user-attachments/assets/48cc11fe-9060-4dcd-ac90-3d8ad97ebf5f)
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
![image](https://github.com/user-attachments/assets/88961458-50c9-419f-b2fb-5630cb55c630)
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
![image](https://github.com/user-attachments/assets/18307f5c-ff8b-452e-b937-ab29449b8217)
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
![image](https://github.com/user-attachments/assets/4e021a4e-eae9-4ec2-a440-a5e698d135a2)
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
![image](https://github.com/user-attachments/assets/3377115e-6acd-44c3-8743-a9020ffb02fb)
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
![image](https://github.com/user-attachments/assets/fdcfedc1-3fe2-477e-8dfb-d33866cdc938)
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
![image](https://github.com/user-attachments/assets/40d81481-118a-4d07-ae00-de7dbf4ee2de) 
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
## OUTPUT
![image](https://github.com/user-attachments/assets/b9a8ddec-c3a7-4a71-8276-e323a7656a0d)
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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
![image](https://github.com/user-attachments/assets/1d991c93-46ac-4e26-a9d4-0eb045fac9f6)
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
![image](https://github.com/user-attachments/assets/d0ca29e8-720c-43f0-9d75-b3aea36ccc1d)
 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/2c38d118-554d-423a-8cf5-8d990df2641b)
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
 ![image](https://github.com/user-attachments/assets/72d95dd0-680f-4b2e-813f-1707d1e4a985)
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
 ./argshift.sh 1 2 3
 ![image](https://github.com/user-attachments/assets/887981de-e13e-4c52-acf1-d822d408dfda)
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
![image](https://github.com/user-attachments/assets/df10cddd-136b-4244-85c0-e6d39f7c7456)
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
![image](https://github.com/user-attachments/assets/1a1dabf2-4363-4573-ba85-9d97e37e2627)
# RESULT:
The Commands are executed successfully.
