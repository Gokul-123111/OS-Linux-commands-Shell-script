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
<img width="950" height="148" alt="image" src="https://github.com/user-attachments/assets/490a52f8-9873-4da7-b918-f6f9dfaf870f" />



cat < file2
## OUTPUT
<img width="891" height="172" alt="image" src="https://github.com/user-attachments/assets/0ea3ff01-9d8a-45a9-92fb-e771fc48a323" />


# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT
<img width="976" height="579" alt="image" src="https://github.com/user-attachments/assets/7089eeec-ae7e-4fdd-aac7-68b782c2000b" />


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
<img width="946" height="448" alt="image" src="https://github.com/user-attachments/assets/69342552-15c3-44e8-b416-083dfd6d61c0" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="946" height="448" alt="os_exp01_5" src="https://github.com/user-attachments/assets/4447f606-d7ed-4eed-af51-1362b5f05091" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="922" height="130" alt="os_exp01_6" src="https://github.com/user-attachments/assets/5acb8d94-0680-4e40-8ccb-95ef4a55bc4b" />


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

<img width="918" height="174" alt="os_exp01_7" src="https://github.com/user-attachments/assets/b66a097e-2dd1-408b-b77f-849a7f0456fe" />


grep hello newfile 
## OUTPUT

<img width="927" height="80" alt="os_exp01_8" src="https://github.com/user-attachments/assets/2b9f3216-1286-4c16-8ad1-f71733f1780d" />



grep -v hello newfile 
## OUTPUT

<img width="895" height="77" alt="os_exp01_9" src="https://github.com/user-attachments/assets/cdc5dd18-f9e5-4bbf-a7af-4da5f0cd9151" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="913" height="102" alt="os_exp01_10" src="https://github.com/user-attachments/assets/c56ff71e-cd2e-40df-b4ad-0b0431710758" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="902" height="78" alt="os_exp01_11" src="https://github.com/user-attachments/assets/a759988f-3ef0-4df9-981c-6a7a5d5e8737" />



grep -R ubuntu /etc
## OUTPUT

<img width="980" height="81" alt="os_exp01_12" src="https://github.com/user-attachments/assets/632518b9-114b-42d0-87b2-0ad3ecd627e9" />


grep -w -n world newfile   
## OUTPUT

<img width="949" height="103" alt="os_exp01_13" src="https://github.com/user-attachments/assets/d7537218-a8b0-4ae2-886e-d6985161aee5" />

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

<img width="986" height="444" alt="os_exp01_14" src="https://github.com/user-attachments/assets/7c5a03ba-5614-481d-b945-a81741b49e03" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="946" height="105" alt="os_exp01_15" src="https://github.com/user-attachments/assets/2fb1553d-3cc3-4860-a7a1-b5323a27c564" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="912" height="95" alt="os_exp01_16" src="https://github.com/user-attachments/assets/17683aca-a416-4c0e-b485-56adffa28d9d" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="922" height="77" alt="os_exp01_17" src="https://github.com/user-attachments/assets/5aeead37-5cc0-447e-bb49-025e32178038" />



egrep '(world$)' newfile 
## OUTPUT

<img width="924" height="102" alt="os_exp01_18" src="https://github.com/user-attachments/assets/8ed025ca-b0e5-4c8d-9af0-280b89d26a1d" />


egrep '(World$)' newfile 
## OUTPUT
<img width="949" height="81" alt="os_exp01_19" src="https://github.com/user-attachments/assets/afedffe9-ffd7-417d-b6a8-9ae1de7ff8f9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="939" height="129" alt="os_exp01_20" src="https://github.com/user-attachments/assets/1c3639bc-2680-4925-a63f-a3acca2d7181" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="894" height="81" alt="os_exp01_21" src="https://github.com/user-attachments/assets/b65441ab-9082-44b2-be6d-0f374b743a2b" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="921" height="73" alt="os_exp01_22" src="https://github.com/user-attachments/assets/89caa649-d07d-4c36-86f3-1ce4f027e45f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="916" height="74" alt="os_exp01_23" src="https://github.com/user-attachments/assets/3ce60dcb-e922-4ff5-8d59-d8869346fcdd" />


egrep l{2} newfile
## OUTPUT
<img width="907" height="102" alt="os_exp01_24" src="https://github.com/user-attachments/assets/522a3163-67e5-473f-bacc-ef67facdb35a" />



egrep 's{1,2}' newfile
## OUTPUT 


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

<img width="910" height="329" alt="os_exp01_26" src="https://github.com/user-attachments/assets/24d5a978-6de7-4690-aa9f-23bda211390c" />


sed -n -e '$p' file23
## OUTPUT

<img width="922" height="84" alt="os_exp01_27" src="https://github.com/user-attachments/assets/5ea0d01a-c7b2-4868-b5cb-784d7133b810" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="897" height="250" alt="os_exp01_28" src="https://github.com/user-attachments/assets/bfe8fa56-5c47-4a2a-a7d8-c5299c042372" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="914" height="249" alt="os_exp01_30" src="https://github.com/user-attachments/assets/572f5a76-8842-48f4-abc0-93343f4051c0" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="929" height="247" alt="os_exp01_31" src="https://github.com/user-attachments/assets/5e691db7-285c-4c0b-bd2e-b241efafde10" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="919" height="175" alt="os_exp01_32" src="https://github.com/user-attachments/assets/999cb3c7-a5d7-4c03-958a-eafb0adb9280" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="918" height="125" alt="os_exp01_33" src="https://github.com/user-attachments/assets/7ef6a926-4bf9-4fea-9713-fe732d4d16f3" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="925" height="101" alt="os_exp01_34" src="https://github.com/user-attachments/assets/444bddda-1277-482b-b8b0-a93289a7efc5" />


seq 10 
## OUTPUT

<img width="920" height="298" alt="os_exp01_35" src="https://github.com/user-attachments/assets/9692699a-e88f-4a36-b90e-0e0f194ffc0b" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="903" height="123" alt="os_exp01_36" src="https://github.com/user-attachments/assets/cdb98f39-0fcf-43cd-a368-19d30f0eb190" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="901" height="137" alt="os_exp01_37" src="https://github.com/user-attachments/assets/8e618b9f-b550-42d5-aa3d-e989741f4b41" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="920" height="150" alt="os_exp01_38" src="https://github.com/user-attachments/assets/38ff8dfb-ce65-4e4b-abdb-14084523f35c" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="908" height="119" alt="os_exp01_39" src="https://github.com/user-attachments/assets/9b3d98c5-24bf-4371-a2ec-c1f757a240bf" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="924" height="120" alt="os_exp01_40" src="https://github.com/user-attachments/assets/e827bbf2-6d0b-4eaf-9770-7f7f0ffe1067" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="922" height="126" alt="os_exp01_41" src="https://github.com/user-attachments/assets/9728996c-544c-4b48-a543-79a139a53a9a" />



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
<img width="926" height="466" alt="os_exp01_42" src="https://github.com/user-attachments/assets/d8ce3212-4fc1-480e-8cf5-e449442682ea" />


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

<img width="913" height="371" alt="os_exp01_43" src="https://github.com/user-attachments/assets/06ed5eab-993c-4357-a9e5-1a5ca23d82bf" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="927" height="242" alt="os_exp01_44" src="https://github.com/user-attachments/assets/c15b244c-4bc7-4992-a34c-c3c5d4b670b5" />

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

<img width="925" height="375" alt="os_exp01_45" src="https://github.com/user-attachments/assets/f9c5ad98-6431-4658-a0c3-96f4916e98f2" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="902" height="125" alt="os_exp01_46" src="https://github.com/user-attachments/assets/8b9a1b28-5d16-47c2-a772-d1053974900b" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="922" height="252" alt="os_exp01_47" src="https://github.com/user-attachments/assets/63fad401-9382-4c17-9542-815d0bea488d" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="917" height="350" alt="os_exp01_48" src="https://github.com/user-attachments/assets/f0aeb521-df85-441f-810c-05d8c164cb36" />


tar -xvf backup.tar
## OUTPUT
<img width="927" height="219" alt="os_exp01_49" src="https://github.com/user-attachments/assets/0ea21018-bc9f-4743-b26c-b7bd08e3c052" />


gzip backup.tar


ls .gz
## OUTPUT
 <img width="923" height="109" alt="os_exp01_50" src="https://github.com/user-attachments/assets/3c3db222-ff7b-44d9-8aeb-42183b33392b" />

gunzip backup.tar.gz
## OUTPUT
<img width="909" height="47" alt="os_exp01_51" src="https://github.com/user-attachments/assets/510b2a56-9cee-4683-82f5-3aeddda059a6" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="886" height="154" alt="os_exp01_52" src="https://github.com/user-attachments/assets/874cc98b-e2ab-4b95-81f6-3682883b50e7" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="914" height="272" alt="os_exp01_53" src="https://github.com/user-attachments/assets/cd778185-6dec-4f7a-a17b-eb120f3432eb" />

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

 <img width="687" height="767" alt="os_exp01_54" src="https://github.com/user-attachments/assets/5a4d65cd-e667-478d-b876-54e1d440250b" />
ls file1
## OUTPUT
<img width="634" height="54" alt="os_exp01_55" src="https://github.com/user-attachments/assets/a4adb8e4-bdd1-423f-812d-b71d74218ba3" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="661" height="106" alt="os_exp01_57" src="https://github.com/user-attachments/assets/0d92ef53-ee3f-4e91-b933-7351c373ef5f" />

abcd
 
echo $?
 ## OUTPUT

<img width="638" height="103" alt="os_exp01_58" src="https://github.com/user-attachments/assets/117e01fa-fc22-496b-9d66-a5cdcde02c14" />

 
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
<img width="693" height="457" alt="os_exp01_59" src="https://github.com/user-attachments/assets/3994fc11-2d08-4ee8-ac7f-495ea5db39de" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
<img width="768" height="361" alt="os_exp01_60" src="https://github.com/user-attachments/assets/97c1f69a-17d0-497f-828f-e32a37d8729b" />

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
<img width="920" height="701" alt="os_exp01_61" src="https://github.com/user-attachments/assets/ad445d76-e481-4729-a21f-b509b6edc50e" />



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
<img width="696" height="535" alt="os_exp01_62" src="https://github.com/user-attachments/assets/254adcb7-2281-43f9-9792-576b4d123f11" />


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
<img width="739" height="820" alt="os_exp01_64" src="https://github.com/user-attachments/assets/dd3a2858-9e2c-4bb5-b0e6-bba3ce6d5c01" />


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
<img width="685" height="189" alt="os_exp01_65" src="https://github.com/user-attachments/assets/1ffc8ae5-b58d-4df6-972b-f976fe5da8b1" />


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
<img width="685" height="189" alt="os_exp01_65" src="https://github.com/user-attachments/assets/becdb4b2-8d4b-4da9-b68c-8da828b999e1" />

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
 <img width="742" height="305" alt="os_exp01_66" src="https://github.com/user-attachments/assets/ae7a5f20-a8d0-44bd-ae64-f2935d4c2237" />

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
 
 <img width="700" height="338" alt="os_exp01_68" src="https://github.com/user-attachments/assets/ce8a27ba-a780-401d-912f-672494694951" />

 
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
<img width="773" height="220" alt="os_exp01_70" src="https://github.com/user-attachments/assets/f80a953e-5ead-4b9b-8b13-f268c4bd122b" />

## OUTPUT
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

<img width="675" height="441" alt="os_exp01_71" src="https://github.com/user-attachments/assets/b60af882-5fe1-4236-b816-f9917ce18922" />

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
<img width="710" height="314" alt="os_exp01_72" src="https://github.com/user-attachments/assets/5bd05251-3155-41b9-9bcf-5ce2503c99d2" />

cat for
ctype1.sh 
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
<img width="734" height="224" alt="os_exp01_73" src="https://github.com/user-attachments/assets/858d802b-07e5-4e12-8fe8-d810a4cc57cb" />

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
<img width="657" height="677" alt="os_exp01_74" src="https://github.com/user-attachments/assets/82a22584-c9bc-4eca-be48-735f02d5def4" />

 
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
<img width="730" height="345" alt="os_exp01_75" src="https://github.com/user-attachments/assets/ea22713c-f23c-4b18-b205-654a39d838a4" />

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
 <img width="993" height="340" alt="os_exp01_76" src="https://github.com/user-attachments/assets/28eb17ce-5124-4189-ab91-134e95718daa" />

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
<img width="975" height="77" alt="os_exp01_77" src="https://github.com/user-attachments/assets/77bab980-16e1-484c-95db-f8c6451de657" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="899" height="100" alt="os_exp01_78" src="https://github.com/user-attachments/assets/19fa518e-dca3-49c0-a1ae-7b1d31c781eb" />


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
<img width="963" height="506" alt="os_exp01_79" src="https://github.com/user-attachments/assets/af5ce3d7-acf7-4fe7-915f-fc528dcac6ed" />

 
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
 <img width="923" height="469" alt="os_exp01_81" src="https://github.com/user-attachments/assets/f596e02d-b64c-4ce0-b1ef-0af722fa1000" />

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
 
 <img width="905" height="620" alt="os_exp01_82" src="https://github.com/user-attachments/assets/7f60225f-2a69-4b86-b749-0a347fd173ee" />

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
 <img width="901" height="379" alt="os_exp01_83" src="https://github.com/user-attachments/assets/ad2f07e0-f0ca-433b-b20e-1e659883ddbd" />

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
<img width="994" height="602" alt="os_exp01_84" src="https://github.com/user-attachments/assets/4c5fdfdd-7b26-4917-b1fe-9ea97a3bccb5" />


# RESULT:
The Commands are executed successfully.
