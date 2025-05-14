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

![1](https://github.com/user-attachments/assets/7eb70697-3d26-485c-a905-3acdc2cbdefc)


cat < file2
## OUTPUT
![2](https://github.com/user-attachments/assets/e3b2781f-6b07-4c7a-9dc4-c96e741d322d)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![3](https://github.com/user-attachments/assets/f6ba0a81-c2f2-461f-8a8d-aaf4dacf2ffb)

comm file1 file2
 ## OUTPUT
![4](https://github.com/user-attachments/assets/2587e84e-d484-4a8a-abb3-c04bd31f02c1)

 
diff file1 file2
## OUTPUT
![5](https://github.com/user-attachments/assets/08f8d0ef-e232-45d5-9583-a1fa1258d494)


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

![6](https://github.com/user-attachments/assets/bd10cc7a-8498-4752-b48c-3f3e51769e64)



cut -d "|" -f 1 file22
## OUTPUT

![7](https://github.com/user-attachments/assets/2dc05892-fc72-4f7f-8e24-ee7898bc8e24)


cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/user-attachments/assets/5c7d7b5a-69a4-47cd-9145-b6a179c6f3ad)


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

![9](https://github.com/user-attachments/assets/10bb3c7c-7a7f-4778-8c5b-619aaee1b899)


grep hello newfile 
## OUTPUT

![10](https://github.com/user-attachments/assets/df1c3614-1182-4773-811a-4fd8a33d4c7a)



grep -v hello newfile 
## OUTPUT

![11](https://github.com/user-attachments/assets/7c73133d-680e-4652-9e0d-40d5b9861109)


cat newfile | grep -i "hello"
## OUTPUT
![12](https://github.com/user-attachments/assets/f5acd5fc-20ea-4d1d-afd7-8787d9816a7e)

cat newfile | grep -i -c "hello"
## OUTPUT

![12](https://github.com/user-attachments/assets/5f2c0861-edd2-4d4f-9c17-4b1fed673638)



grep -R ubuntu /etc
## OUTPUT

![14](https://github.com/user-attachments/assets/7fb1328f-35bb-4b8c-8b41-ce8d61297053)


grep -w -n world newfile   
## OUTPUT

![15](https://github.com/user-attachments/assets/d5f90dce-1e4d-4bfd-8f00-7305d382cb70)

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

![16](https://github.com/user-attachments/assets/dbd8b426-43ff-431a-9026-2e60f81f1567)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![17](https://github.com/user-attachments/assets/e9e1ab59-3da5-41ef-897d-ef5395bc9fcd)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![18](https://github.com/user-attachments/assets/559b555b-f477-4638-b3ae-afaa8696b86e)



egrep '(^hello)' newfile 
## OUTPUT

![19](https://github.com/user-attachments/assets/5c2e3612-b233-4200-a94c-2bb3e8e0e7a3)


egrep '(world$)' newfile 
## OUTPUT

![20](https://github.com/user-attachments/assets/e55c047a-2217-4282-bbf4-2bd5cb8bec37)


egrep '(World$)' newfile 
## OUTPUT

![21](https://github.com/user-attachments/assets/ad5eb805-56e9-4964-84b9-875639a8ae8e)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![22](https://github.com/user-attachments/assets/7ab1b5a2-e9d1-45f6-8478-2c97c61bf2f3)


egrep '[1-9]' newfile 
## OUTPUT

![23](https://github.com/user-attachments/assets/f7d4d856-2c5d-4149-a80c-23be8104065a)


egrep 'Linux.*world' newfile 
## OUTPUT

![24](https://github.com/user-attachments/assets/ec64cec1-b5e3-4cea-b8e3-68c0ac816111)

egrep 'Linux.*World' newfile 
## OUTPUT

![25](https://github.com/user-attachments/assets/9c6115ec-13c4-429a-92bf-895ef3d754ec)

egrep l{2} newfile
## OUTPUT

![26](https://github.com/user-attachments/assets/304e3c24-be46-48cb-ba75-797a91b77b3d)


egrep 's{1,2}' newfile
## OUTPUT 
![27](https://github.com/user-attachments/assets/369f2105-02a4-42c9-abda-b85d76af5c62)


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

![28](https://github.com/user-attachments/assets/45eb0398-a7a4-451e-86ce-28cf681050d1)


sed -n -e '$p' file23
## OUTPUT

![29](https://github.com/user-attachments/assets/81d7f86e-b4b6-4414-808f-f0641c3a87db)

sed  -e 's/Ram/Sita/' file23
## OUTPUT

![30](https://github.com/user-attachments/assets/7102221a-e520-40df-b317-7c1a6504d861)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![31](https://github.com/user-attachments/assets/8d837f28-9356-4d11-b6ee-945afae2a727)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![32](https://github.com/user-attachments/assets/23e5d0c6-5f94-4b02-ae38-f4eccbeeeb79)

sed -n -e '1,5p' file23
## OUTPUT

![33](https://github.com/user-attachments/assets/238af426-465b-4b9b-8a93-e1997587856e)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![34](https://github.com/user-attachments/assets/a668231b-2bf1-4755-9698-0edf36fdb2ab)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![35](https://github.com/user-attachments/assets/68e8aa53-7097-432d-bd48-0d8f789b4b4f)


seq 10 
## OUTPUT

![36](https://github.com/user-attachments/assets/4c34b578-b095-42eb-8836-be4381d7ac44)


seq 10 | sed -n '4,6p'
## OUTPUT

![37](https://github.com/user-attachments/assets/dc44b10a-b020-43cf-9cce-92c4882e4528)


seq 10 | sed -n '2,~4p'
## OUTPUT

![38](https://github.com/user-attachments/assets/f62017df-20ff-492f-b642-eaee967c31a6)


seq 3 | sed '2a hello'
## OUTPUT

![39](https://github.com/user-attachments/assets/8612b44c-0606-4f9d-a565-5e7fc7ec0059)


seq 2 | sed '2i hello'
## OUTPUT
![40](https://github.com/user-attachments/assets/b5caca28-2289-4c26-ba16-031009916b44)


seq 10 | sed '2,9c hello'
## OUTPUT

![41](https://github.com/user-attachments/assets/1ecd3c4f-08c2-4236-a4ed-896bb8b75f42)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![42](https://github.com/user-attachments/assets/a98291f9-58c6-4e80-95fa-c82afd7dbfa3)


sed -n '2,4{s/$/*/;p}' file23
![43](https://github.com/user-attachments/assets/b16daab9-87ee-47cf-970d-107d71a49471)


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
![44](https://github.com/user-attachments/assets/bdcd9d74-ff58-41d0-b936-84ba5210dd0c)


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
![45](https://github.com/user-attachments/assets/8a22cd2b-56aa-41f0-8cbb-6785eab723ae)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![46](https://github.com/user-attachments/assets/ae934aa3-af97-41e0-a6fa-735c4e12e6c0)

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
![47](https://github.com/user-attachments/assets/f3159f36-69b8-4eee-b59c-d182cc332f23)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![48](https://github.com/user-attachments/assets/b7c696da-5e21-4896-b32f-1adc49400b1b)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![back](https://github.com/user-attachments/assets/de27dbdb-c113-4fbd-9cb9-c745cc65cf77)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![backup1](https://github.com/user-attachments/assets/0d70c589-07b2-400a-98ec-e0d4fc869a55)


tar -xvf backup.tar
## OUTPUT
![backup2](https://github.com/user-attachments/assets/1200b789-85a1-4adf-8321-16f318b02f83)

gzip backup.tar

ls .gz
## OUTPUT
 ![gz1](https://github.com/user-attachments/assets/3cb1ea8d-7b6d-43ec-a63d-5f29e5761846)

gunzip backup.tar.gz
## OUTPUT
![gz2](https://github.com/user-attachments/assets/c7a75a54-a4a3-49ac-9ca4-88a576b23456)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![50 - shell script](https://github.com/user-attachments/assets/6d3b987d-db39-4865-b76c-1200d6ef2179)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![51](https://github.com/user-attachments/assets/40f71c47-308f-444b-95eb-39a0688e13e7)


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
![52](https://github.com/user-attachments/assets/095e0ab5-8375-4c77-bb4f-111972cc0da3)

 
ls file1
## OUTPUT
![53](https://github.com/user-attachments/assets/6e374e32-c101-484d-9cf7-8b931ab6f3c6)

echo $?
## OUTPUT 
![54](https://github.com/user-attachments/assets/4b1638ab-2279-4ada-a900-798a47bbd3d1)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![55](https://github.com/user-attachments/assets/a1cf97fa-3b1d-4e83-844e-272ac5e41b96)

abcd
 
echo $?
 ## OUTPUT
![56](https://github.com/user-attachments/assets/db2a6ef5-d4de-4f8b-96f0-c87bb97f585d)


 
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
![57](https://github.com/user-attachments/assets/7c6cf327-55b6-4ca3-83c5-923e3de730d6)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![58](https://github.com/user-attachments/assets/7fd603df-4a4d-4287-b1fe-c3b90f352882)


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
![59](https://github.com/user-attachments/assets/e5e8fd93-6344-45e3-a932-2f8a41e9deef)


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
![60](https://github.com/user-attachments/assets/18086439-3040-4916-8352-7cdb5ab91e59)



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
![1_](https://github.com/user-attachments/assets/d1b973e7-2da8-4608-8ec3-ec9dd3766001)


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
![61](https://github.com/user-attachments/assets/b1a34fcf-1712-4db6-9dd7-0f2f198dc85e)

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
![62](https://github.com/user-attachments/assets/9457e185-4885-4c19-afe7-48dbdf291558)


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
![63](https://github.com/user-attachments/assets/d664dad5-0a74-4960-b253-e3b6cab94520)

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
 
 ![65](https://github.com/user-attachments/assets/23e424a1-2507-42a6-84ae-79d8bf52abdc)

 
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
 
 ![66](https://github.com/user-attachments/assets/4e5e786c-dfec-4206-8c1e-37103e7f2f14)

 
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
 
 ![67](https://github.com/user-attachments/assets/9dfa87bd-d803-4f5f-af79-ae90f2bae582)

 
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
 ![68](https://github.com/user-attachments/assets/edf8544c-ad94-4568-bc5a-8c3f0aa96dbe)

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
 ![69](https://github.com/user-attachments/assets/0ca21160-2070-40de-9e16-44d9f6c88108)

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
![70](https://github.com/user-attachments/assets/42c6d934-dafb-4706-a4a5-1f6d3a16e5a2)

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
![71](https://github.com/user-attachments/assets/e73dc581-5384-44c3-96d9-cfd548cd12c4)


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
![72](https://github.com/user-attachments/assets/7420bd37-84b8-45dd-8ed1-0c6e22cb5bd5)

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
![73](https://github.com/user-attachments/assets/326e4d07-f642-4fda-902e-75e38edb2a2a)

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
![74](https://github.com/user-attachments/assets/842f1a87-8484-474a-8029-614e051f70f7)


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
![75](https://github.com/user-attachments/assets/763f3f9f-66f9-45c7-a4ac-3dfcc9749cb2)


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
 ![76](https://github.com/user-attachments/assets/3ea01f54-1d8e-4f2f-aae2-5c4039a60e2a)

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![](img/sem%20i75.png)


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

 ![79](https://github.com/user-attachments/assets/c4664977-ee12-471c-a476-35203c49759f)

 ./funcex.sh 1 2

 ![80](https://github.com/user-attachments/assets/aed6f18f-b7f1-461f-bc3a-ebc3254cd198)

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
 ![81](https://github.com/user-attachments/assets/8ed3567d-b4b0-4bc9-850e-4558b76f194e)

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
 ![82](https://github.com/user-attachments/assets/34d40ce6-81cf-4187-8d11-ce0062bf6889)

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
 ![83](https://github.com/user-attachments/assets/8893aebb-ef88-442a-85f9-7e8a48e06032)

 
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
 ![84](https://github.com/user-attachments/assets/1d0c36d4-37e9-47ad-ad3b-3b4eccb5a6c9)

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

![85](https://github.com/user-attachments/assets/99a43e72-bded-4e02-b65b-bf30c4dda53e)

# RESULT:
The Commands are executed successfully.
