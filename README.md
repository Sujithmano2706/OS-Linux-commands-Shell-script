
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
<img width="363" height="112" alt="589364159-62dde542-1570-40bc-9ba3-7da210e9db7b" src="https://github.com/user-attachments/assets/995b01e8-ca17-407c-b9e7-122fd095adb1" />
<img width="363" height="112" alt="589364159-62dde542-1570-40bc-9ba3-7da210e9db7b" src="https://github.com/user-attachments/assets/24601f78-0888-422d-9ed9-50d463bdec04" />
cat < file2
## OUTPUT
<img width="373" height="136" alt="589364289-b05e2079-9d9d-4481-8cf1-d4c534e70816" src="https://github.com/user-attachments/assets/cf35722f-d865-49ef-a190-e48af544a0ed" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="461" height="50" alt="589364654-56acd36b-3140-404a-9db9-a93a8bd61c71" src="https://github.com/user-attachments/assets/78010c6c-acd1-4773-84e7-ca7f3e3cff4b" />

comm file1 file2
 ## OUTPUT
<img width="481" height="237" alt="589364735-ee4f5ec0-595f-4ddc-ba3f-211c0ed58a27" src="https://github.com/user-attachments/assets/9a27a6dd-f284-4916-9452-2bc18b9b8530" />

 
diff file1 file2
## OUTPUT

<img width="381" height="268" alt="589364833-7e80c958-5068-4356-ae48-c9e6b9fcb971" src="https://github.com/user-attachments/assets/b0f66feb-a151-4543-9829-41312f818f3e" />

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
<img width="348" height="62" alt="589364956-600e8563-f157-4803-8c34-54387335501a" src="https://github.com/user-attachments/assets/aa2217cd-0a5b-4dd0-b355-6088e6bcb5f6" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="440" height="92" alt="589365060-f811cf86-84b4-46d4-9978-a1f0f5964299" src="https://github.com/user-attachments/assets/2f39c57e-fb19-4a08-abef-2762a769d7b0" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="422" height="87" alt="589365155-12f9e481-413b-40ad-8bd2-96f248b046c5" src="https://github.com/user-attachments/assets/b1e4eea6-d974-4f3a-a8e4-b0f3ce015418" />

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

<img width="337" height="46" alt="589365256-88b9cbe5-9c21-4692-886e-c397adfb1a7a" src="https://github.com/user-attachments/assets/44b82577-046a-48f4-b72a-6c03128a5ee0" />


grep hello newfile 
## OUTPUT
<img width="342" height="45" alt="589365342-e7c32bda-37e0-4f5e-96cd-199a0e4bfa0a" src="https://github.com/user-attachments/assets/5177214f-9b0e-4d07-bcb3-d61ae74d26ab" />




grep -v hello newfile 
## OUTPUT

<img width="367" height="41" alt="589365411-f314ff2c-7999-43f2-83f8-bb9341a8c373" src="https://github.com/user-attachments/assets/ef52f820-06a4-4cf2-abe8-a0d576bf8b37" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="466" height="70" alt="589365488-3ec78633-e12d-452f-a19c-1193c96e0cb1" src="https://github.com/user-attachments/assets/edcb3afc-5de6-4105-914d-78cb482621ca" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="547" height="44" alt="589365565-4e34a3d2-b14a-427a-bc1c-3d54c89afd6b" src="https://github.com/user-attachments/assets/9417f4c3-b448-4dbc-abed-37cab4922f6b" />


grep -w -n world newfile   
## OUTPUT

<img width="508" height="72" alt="589365657-35d14406-8a58-4639-8ea2-f6b422bb66de" src="https://github.com/user-attachments/assets/ef1946eb-8962-442c-a8c7-d5d820ad0551" />

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
<img width="478" height="63" alt="589365755-0f5198e6-81db-451d-8809-49208f321dc1" src="https://github.com/user-attachments/assets/58b4e999-7096-4937-a619-75e305838d45" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="470" height="63" alt="589365808-7b93e299-a2c7-4b42-9561-6bd0e53ff179" src="https://github.com/user-attachments/assets/c45612f3-d7f2-46ac-940f-81015a59dbf0" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="533" height="67" alt="589365872-502a552a-908b-4672-b681-2bf04955bca1" src="https://github.com/user-attachments/assets/5ed3c2cd-2c4a-4feb-a5d1-87e64286ba22" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="428" height="48" alt="589365952-7ce9825c-5c35-4dba-9752-bb5e882d86e0" src="https://github.com/user-attachments/assets/988f3952-3f81-4e34-816c-f1c677a432e2" />



egrep '(world$)' newfile 
## OUTPUT

<img width="419" height="91" alt="589366043-951019cc-21ea-4dcf-ac1a-ba7b376ffcf3" src="https://github.com/user-attachments/assets/3b959047-7e7f-412b-a2ae-9b7af5cbbed9" />


egrep '(World$)' newfile 
## OUTPUT
<img width="419" height="91" alt="589366199-842b487d-8e5d-4973-91b4-206f9cd0bd77" src="https://github.com/user-attachments/assets/883a00e6-075e-4b34-96de-32ce95b6becf" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="488" height="87" alt="589366299-712f935c-e113-40c9-a266-f06e079bd26c" src="https://github.com/user-attachments/assets/d5ed1f56-4a24-46bf-9645-2b50bc56a72d" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="431" height="43" alt="589366391-f2311fc2-0135-4f78-8365-ebaf3fb22608" src="https://github.com/user-attachments/assets/0d6f6c27-e09e-4e8a-b621-ef0a9f04b39b" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="503" height="63" alt="589366491-7594b973-0127-4f75-a1f9-3602556e3e82" src="https://github.com/user-attachments/assets/7cdb7eb9-6920-45af-bc3d-adb150672d4c" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="503" height="63" alt="589366491-7594b973-0127-4f75-a1f9-3602556e3e82" src="https://github.com/user-attachments/assets/30482f1f-9352-4afe-b884-c8cdb45a7d99" />


egrep l{2} newfile
## OUTPUT
<img width="503" height="63" alt="589366743-8d32b953-6f56-402f-a0e8-da7c5c2b9e55" src="https://github.com/user-attachments/assets/0ead0641-19dc-4a54-9aba-c68d882dd136" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="394" height="63" alt="589366624-2b088be1-6413-4318-83ed-1e284b711563" src="https://github.com/user-attachments/assets/2233a4ba-8660-49f0-9a0a-5a5fda76cc1d" />


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
<img width="395" height="41" alt="589366964-271bdac6-4de3-4711-b27b-234bb5a9b966" src="https://github.com/user-attachments/assets/3a740688-a2ad-47b1-bd7c-80bb4968e13e" />



sed -n -e '$p' file23
## OUTPUT
<img width="384" height="44" alt="589367072-3319f46c-09f7-4b56-a722-79c76cd1b201" src="https://github.com/user-attachments/assets/274a8473-6c44-4988-a11a-02b6dde7e03d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="482" height="197" alt="589367165-a818b718-464f-4d3b-8aeb-bec77d1e67a8" src="https://github.com/user-attachments/assets/3eb8ab6d-0d48-4abe-b8b1-458c6e351df5" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="510" height="195" alt="589367252-502f6a4a-2904-49e1-b422-fb3c51780538" src="https://github.com/user-attachments/assets/47cf17a0-d8b4-40f0-a5ec-e99b40bb1583" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="490" height="198" alt="589367350-016e844f-7b2f-4b73-b661-9e0cd2bf43f6" src="https://github.com/user-attachments/assets/6fe97bcc-7a7e-4231-8e4b-415f599a8ece" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="481" height="87" alt="589367440-210b00c5-a78a-4d13-9ae0-982eb8e6073d" src="https://github.com/user-attachments/assets/2fbb6885-9c2a-40c2-b4ee-0e526695c6c6" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="481" height="87" alt="589367635-db7d5a13-97fb-46d2-9a82-dcd71072e0a3" src="https://github.com/user-attachments/assets/ff4c60d7-1958-4998-8576-5408201e02d5" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="471" height="73" alt="589367699-1d904f00-f068-4a8c-955d-911c8b0f6576" src="https://github.com/user-attachments/assets/db26a587-5df5-4aba-b273-1cc2a3a17c30" />



seq 10 
## OUTPUT
<img width="348" height="247" alt="589367748-a08b7144-2bd2-46ea-b056-41b14109beaa" src="https://github.com/user-attachments/assets/19c6ee52-1825-4983-bf59-d2f1cd01af65" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="437" height="89" alt="589367836-8c6e7fed-6797-46b9-ae0a-ece4ed9514e8" src="https://github.com/user-attachments/assets/ca989c8e-b2e8-45cb-9138-e8336b9ffdba" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="432" height="88" alt="595269359-b3255a23-9a25-4655-a302-248f2b644d36" src="https://github.com/user-attachments/assets/7d6d6ad3-908a-4dfc-aa61-39412228678a" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="414" height="109" alt="589367999-d912d748-082c-4b72-b0e8-c24cef0f8715" src="https://github.com/user-attachments/assets/86a700c6-1fa5-434d-8677-5e3ec16f7d87" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="435" height="86" alt="589368051-93ad4c75-129b-4b44-873c-6e91231f0d16" src="https://github.com/user-attachments/assets/70e6c2d8-2d63-4bfc-8878-4956a24347e2" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="432" height="88" alt="595271184-adc703b2-38d9-4e79-97f3-a9c73c5eff1c" src="https://github.com/user-attachments/assets/ee59d73b-6fc2-4b55-b0a4-fbb7a806328a" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="591" height="87" alt="595271317-730cba3d-68dd-4cbb-8a9c-e768ca8540a9" src="https://github.com/user-attachments/assets/7b78f133-d60f-4fc0-bb15-5da497f073b2" />


sed -n '2,4{s/$/*/;p}' file23
<img width="506" height="87" alt="595272545-c48da0e9-cc91-4dbe-9800-d90b6f840d89" src="https://github.com/user-attachments/assets/58fc8077-a00c-42c1-936a-fdb969e1e775" />


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
<img width="342" height="128" alt="595272663-8c5d4870-5726-48a0-b419-14141c8f11bb" src="https://github.com/user-attachments/assets/7503645d-3e65-4a52-a1ca-fa7a80472dfe" />


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
<img width="327" height="127" alt="595273147-fb12a382-77d8-4ba0-bc62-e85e4ce711f5" src="https://github.com/user-attachments/assets/54bd89de-cddd-4c26-94d6-6c209b63b76a" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="581" height="196" alt="595273621-146dc1b1-7470-4646-85c4-48b846cfe151" src="https://github.com/user-attachments/assets/f4b85534-5469-421a-a1ea-3f1da14b15ac" />

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

<img width="488" height="92" alt="595273721-94a97225-9237-473a-b01b-66c73957e7e8" src="https://github.com/user-attachments/assets/3f1231f7-548f-4078-a0fa-c0862492cb11" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="625" height="82" alt="595273852-3d139603-39c9-4a10-8158-ed238a9f0972" src="https://github.com/user-attachments/assets/2bce4662-cdea-490f-8cb8-764755ccf539" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="450" height="197" alt="595274295-70629588-00c3-4abf-8e7d-de43d8ddee37" src="https://github.com/user-attachments/assets/347d0707-0e2f-4dc7-8009-66d6da588814" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="768" height="192" alt="595274435-aef8952e-4c43-4c34-a204-0a4d7ab19f86" src="https://github.com/user-attachments/assets/4256c17e-4454-4b4b-a392-18fd8e9e529e" />

tar -xvf backup.tar
## OUTPUT
<img width="768" height="192" alt="595274786-c53848a8-9ab2-4084-b703-372542d8ec8f" src="https://github.com/user-attachments/assets/1325698b-d951-4b38-bb17-dd72ac5d358d" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="447" height="83" alt="595274902-cc90b3bc-5d37-4f37-8ad3-cae5ca5586ee" src="https://github.com/user-attachments/assets/9910e225-5c7c-4ed6-a2e5-e6261adb26bd" />

gunzip backup.tar.gz
## OUTPUT
<img width="740" height="67" alt="595275035-30c6668d-7dca-40bb-8e23-327cc6fb11e1" src="https://github.com/user-attachments/assets/67a3aa89-45d6-4fec-8aa5-1e6a243b8f8a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="740" height="67" alt="595275540-3bc3b869-07e4-4ca6-8ddc-70d2347b19e9" src="https://github.com/user-attachments/assets/2d447e51-60ff-4b32-9566-b17e3b6bd154" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="432" height="85" alt="595275873-84875b95-04c6-4656-a1c7-57256141a998" src="https://github.com/user-attachments/assets/be4ce574-7185-409c-a7ed-c0cb0422963a" />


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

 <img width="667" height="631" alt="595276519-8e0d086b-3f2b-4773-9a02-201697cc20ac" src="https://github.com/user-attachments/assets/ac45a17e-bb58-45be-806d-804f1aba9821" />

ls file1
## OUTPUT
<img width="405" height="70" alt="595276769-15d1b63e-7847-4b9b-9c4d-bf6885dfc025" src="https://github.com/user-attachments/assets/8a9270f1-20b7-4986-afe4-b6aa29a750af" />

echo $?
## OUTPUT 
<img width="405" height="70" alt="595278750-ac3af9b0-8417-4382-ba0a-37be7f62d694" src="https://github.com/user-attachments/assets/cf16b10e-879b-4678-a496-6457b1c4dc76" />

./onebash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="332" height="38" alt="595279070-ee083df4-d96b-43f7-ac7d-561f88da1134" src="https://github.com/user-attachments/assets/bc3846e8-719c-4375-a999-7da55d808246" />

abcd
 
echo $?
 ## OUTPUT
<img width="362" height="25" alt="595279860-9588b3f8-eb58-4827-8e63-c7dbe763d0ad" src="https://github.com/user-attachments/assets/d7113198-61b4-4724-9897-fe96fb040f01" />
<img width="332" height="38" alt="595279070-ee083df4-d96b-43f7-ac7d-561f88da1134" src="https://github.com/user-attachments/assets/1fb5b7ff-1e6e-448a-b3b4-d3eaca52680d" />


 
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

<img width="362" height="25" alt="595279860-9588b3f8-eb58-4827-8e63-c7dbe763d0ad" src="https://github.com/user-attachments/assets/902f3e0e-0ed2-44c0-964a-6ad3573c05ab" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="362" height="25" alt="595279860-9588b3f8-eb58-4827-8e63-c7dbe763d0ad" src="https://github.com/user-attachments/assets/e7fd7951-cba6-44b8-b856-cf264dc15800" />


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
<img width="452" height="17" alt="595280373-3a963d6b-0a4d-4ef3-ab21-1f1915dbd2cd" src="https://github.com/user-attachments/assets/34226bfc-72a7-4528-aecc-5f3968895cd9" />

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

<img width="461" height="106" alt="595281480-54c7cc3f-fba6-4ed8-b9c6-71c4bde211d5" src="https://github.com/user-attachments/assets/f5e436ee-afaf-4673-8e9b-097e45cdfc49" />


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
<img width="455" height="412" alt="595283506-7c6cea91-8d2a-4b8b-a743-cef622f9d398" src="https://github.com/user-attachments/assets/a318cb96-455a-4b52-b69b-7d150c846cd1" />

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
<img width="387" height="108" alt="595283062-6b6b21e2-1439-4e18-9b43-24775713f3b4" src="https://github.com/user-attachments/assets/be2d6763-664b-4915-af58-be3af72ed19d" />

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

<img width="455" height="30" alt="595283775-8813ec19-0a7d-4991-a593-2519b972a4d0" src="https://github.com/user-attachments/assets/d10674e3-6c4e-4d57-a3da-099b512c957b" />

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
<img width="478" height="65" alt="595284345-d1ed2d0c-301f-4b49-9bf4-ca6a2a14c5b3" src="https://github.com/user-attachments/assets/eaed08ad-48ee-49f4-a599-c3d5c1f221a9" />

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
## output
<img width="478" height="65" alt="595284345-d1ed2d0c-301f-4b49-9bf4-ca6a2a14c5b3" src="https://github.com/user-attachments/assets/5c2bd941-e8dc-4a85-92cd-7f15d60884a8" />

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
 ## output
 <img width="502" height="261" alt="595284740-349a10ee-bda6-462d-9395-5901478af4ab" src="https://github.com/user-attachments/assets/373a7689-49b7-46e8-84c1-b63174bf6bf3" />

 
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
## output
<img width="488" height="135" alt="595285180-1e154c77-a364-4b2d-a3c0-79049b59a8a5" src="https://github.com/user-attachments/assets/4aec2fcf-720d-4a3e-accd-ea1553e5c40e" />

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
## output
<img width="455" height="168" alt="595285553-e3a0bd8a-296a-4062-a2bf-181108af2407" src="https://github.com/user-attachments/assets/390b712c-7fc3-4863-b2bd-f8237159e544" />

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
## output
<img width="476" height="107" alt="595285880-30ffbea5-390d-47dc-b4df-51c7c001c366" src="https://github.com/user-attachments/assets/ef1471bf-06bf-4525-abcf-0467f6d492d9" />


 
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
## output
<img width="476" height="107" alt="595286301-34670640-a482-4e63-a144-e7913ec6b753" src="https://github.com/user-attachments/assets/7878fccc-00cd-403e-9d6c-601eff313d54" />

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
## output
<img width="475" height="177" alt="595286943-d60e2d8f-5453-4021-94c4-14f8ecd768e4" src="https://github.com/user-attachments/assets/3dd4e085-6c8b-49f8-a9b2-2cb511aa2126" />

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
<img width="503" height="202" alt="595287811-20faf6a8-9ee4-4b78-be8d-3808b6210ecf" src="https://github.com/user-attachments/assets/33c0ade6-9f79-46c1-9e4c-8cbabe86e889" />


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

<img width="503" height="202" alt="595287811-20faf6a8-9ee4-4b78-be8d-3808b6210ecf" src="https://github.com/user-attachments/assets/c3e6011d-680a-4edc-91d1-7f75b058bd3b" />

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
<img width="483" height="147" alt="595288425-6614320d-e2e6-4e59-a4e7-9ffd3b9fcdaa" src="https://github.com/user-attachments/assets/1b645a03-6698-42aa-ab49-5b839bc71779" />

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
<img width="613" height="153" alt="595288602-c98c5d0e-3b92-44f8-94fe-4dfc41b5754b" src="https://github.com/user-attachments/assets/c821fa7f-7ae1-4b3d-9104-30db04af892e" />

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

 <img width="613" height="153" alt="595288602-c98c5d0e-3b92-44f8-94fe-4dfc41b5754b" src="https://github.com/user-attachments/assets/d7ec8e0a-23af-47ad-b1c4-01d714436054" />

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
<img width="487" height="307" alt="595288833-9faaa5df-4787-4f86-b9a8-5feab97677d0" src="https://github.com/user-attachments/assets/4b3717d6-5252-4142-958b-f9c6609f6796" />

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
 <img width="497" height="116" alt="595290316-4524aa7a-f5a4-4a92-b77b-eab1d16e8b04" src="https://github.com/user-attachments/assets/3ec8a43f-4d99-4c68-a595-99aa565eb590" />

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
<img width="516" height="155" alt="595290667-cf6950c4-309f-49d3-924d-dc863a23cb15" src="https://github.com/user-attachments/assets/b1b61ad4-35c8-44b2-b486-b15b508bb600" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="595" height="90" alt="595290819-4b28c21d-af0f-4983-854f-87548c8efe06" src="https://github.com/user-attachments/assets/2732103d-ec9f-4992-b981-a88ca59e1655" />


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
<img width="595" height="90" alt="595290819-4b28c21d-af0f-4983-854f-87548c8efe06" src="https://github.com/user-attach
./funcex.sh 1 2 ments/assets/6204ece3-e0dd-4f06-a5d2-93abd4d7098b" />

 <img width="460" height="35" alt="595292254-a76fbde4-fcf4-488e-ae45-61728052a833" src="https://github.com/user-attachments/assets/9ae4fd8f-0ca3-49a5-a333-9b63794095d1" />

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
 <img width="460" height="35" alt="595292254-a76fbde4-fcf4-488e-ae45-61728052a833" src="https://github.com/user-attachments/assets/4b7d061e-629d-4644-b179-157752d1242a" />
<img width="495" height="107" alt="595292829-bf695677-3012-4e9c-b5df-ee4433ba9ca7" src="https://github.com/user-attachments/assets/4579c8da-d880-46db-a4f9-9e5316fe0cf6" />

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
 <img width="560" height="120" alt="595293277-127ddf70-20a2-4fff-b3fb-249ad27dbf26" src="https://github.com/user-attachments/assets/2e6bdd66-ce07-485e-a726-73c426355e81" />

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
 
 <img width="637" height="596" alt="595293604-3fdd3721-17b9-482d-824a-3220579b13e0" src="https://github.com/user-attachments/assets/8b3b6aaa-f196-4b7b-8f5f-5e4248367878" />

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
 <img width="511" height="307" alt="595294481-31d97a6e-d61f-47bb-bbd1-8ec5648e7536" src="https://github.com/user-attachments/assets/071e60f2-23c8-4634-a641-ca9ae0aab5ce" />

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

<img width="500" height="117" alt="595294665-ac8326e0-0126-466b-9d28-3fcbe67e9eaa" src="https://github.com/user-attachments/assets/7253cc78-57e5-4c2b-89a2-a2931d8e65b0" />

# RESULT:
The Commands are executed successfully.
