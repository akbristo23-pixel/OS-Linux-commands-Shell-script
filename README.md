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

<img width="733" height="275" alt="image" src="https://github.com/user-attachments/assets/97462f06-409b-4d14-81bb-e095b20c7bcf" />

cat < file2
## OUTPUT


<img width="994" height="237" alt="image" src="https://github.com/user-attachments/assets/1cc9ae4c-0900-4215-b36a-7faf8a77b80e" />


# Comparing Files
cmp file1 file2
## OUTPUT
  
  <img width="421" height="61" alt="image" src="https://github.com/user-attachments/assets/77b1d5cc-367c-4cdd-8418-b88f17e2de88" />

comm file1 file2
 ## OUTPUT

 <img width="1156" height="432" alt="image" src="https://github.com/user-attachments/assets/66bf1d70-ff30-4bb2-8063-4dc9aae77c88" />

diff file1 file2
## OUTPUT

<img width="1147" height="407" alt="image" src="https://github.com/user-attachments/assets/fed7c9fb-f780-4291-b800-ee9c5dbf4536" />

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

<img width="870" height="162" alt="image" src="https://github.com/user-attachments/assets/87b8ca2e-b223-4ba9-b6bf-8027e89003ce" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="616" height="181" alt="image" src="https://github.com/user-attachments/assets/d8687626-fe82-4aa4-8ae2-01d31f15d131" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="902" height="185" alt="image" src="https://github.com/user-attachments/assets/eb01ba88-10d0-42db-88f2-5a226f21c46b" />


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

<img width="944" height="78" alt="image" src="https://github.com/user-attachments/assets/ecb267df-b0db-44de-9c95-f1a8ee7fd0b3" />

grep hello newfile 
## OUTPUT

<img width="969" height="69" alt="image" src="https://github.com/user-attachments/assets/b38e7f4b-ba88-4582-abe0-986b604ec2d1" />



grep -v hello newfile 
## OUTPUT

<img width="885" height="180" alt="image" src="https://github.com/user-attachments/assets/62d88e7d-cb18-4906-bd18-93b1cc440ddf" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="736" height="96" alt="image" src="https://github.com/user-attachments/assets/68331b4a-0b3e-4e1c-a2a0-70321ba66394" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="619" height="69" alt="image" src="https://github.com/user-attachments/assets/cfee0552-1890-4b28-9831-a7f82269e063" />


grep -R ubuntu /etc
## OUTPUT

<img width="554" height="95" alt="image" src="https://github.com/user-attachments/assets/aa947ffb-df67-44da-8ec5-45d0fcead505" />


grep -w -n world newfile   
## OUTPUT
<img width="1182" height="930" alt="image" src="https://github.com/user-attachments/assets/5ef7143b-06a9-46ba-8821-96790c8d2880" />

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

<img width="710" height="92" alt="image" src="https://github.com/user-attachments/assets/142ccee4-c861-4ab4-b31a-eade39e7b56e" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="542" height="91" alt="image" src="https://github.com/user-attachments/assets/f34eb8d1-f597-4b10-8412-2dcb9a99fefe" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="789" height="92" alt="image" src="https://github.com/user-attachments/assets/d0fa8bb0-b600-4404-9277-f88c12306b58" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="700" height="76" alt="image" src="https://github.com/user-attachments/assets/f99c2b0a-8b75-4a44-b91f-859d4c46924e" />


egrep '(world$)' newfile 
## OUTPUT

<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/4d64eb1f-8392-4432-9e2e-84005098ddf9" />

egrep '(World$)' newfile 
## OUTPUT

<img width="698" height="70" alt="image" src="https://github.com/user-attachments/assets/4962a4ca-fc13-4ed8-806a-9969dd5e15fd" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="854" height="118" alt="image" src="https://github.com/user-attachments/assets/054d6446-b9cc-4580-bf71-cfbd05ca7de4" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="864" height="74" alt="image" src="https://github.com/user-attachments/assets/4ab3f72e-f061-43f0-ad99-035e5d08639e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="680" height="72" alt="image" src="https://github.com/user-attachments/assets/8f7c8112-beca-4512-b983-4a3772f2a1db" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="726" height="68" alt="image" src="https://github.com/user-attachments/assets/69299dfa-ae3d-4167-9cd4-286feaf968ce" />

egrep l{2} newfile
## OUTPUT

<img width="768" height="96" alt="image" src="https://github.com/user-attachments/assets/1ecd9d13-4532-42f2-9ba2-d05a1bf5c27e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="769" height="120" alt="image" src="https://github.com/user-attachments/assets/2a50842c-ae04-489a-ab68-236947eb935a" />

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

<img width="952" height="70" alt="image" src="https://github.com/user-attachments/assets/b00e84d0-a634-46e4-a2ef-b09110e3b468" />

sed -n -e '$p' file23
## OUTPUT

<img width="781" height="72" alt="image" src="https://github.com/user-attachments/assets/895314de-19f8-47a3-af71-c9ec42499353" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="665" height="96" alt="image" src="https://github.com/user-attachments/assets/5a6950d3-546a-4d17-8517-2a2e712f9a3d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="770" height="374" alt="image" src="https://github.com/user-attachments/assets/c946fb04-2efa-4afa-96eb-625ef9485367" />
<img width="859" height="435" alt="image" src="https://github.com/user-attachments/assets/8d13b158-3d57-49c3-bc69-2227f1d9ffc6" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="730" height="415" alt="image" src="https://github.com/user-attachments/assets/3bb7d5ff-b6ae-4a0f-9949-6cabd2e41be2" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="666" height="169" alt="image" src="https://github.com/user-attachments/assets/47a4f27c-72b2-4555-8f92-cedcf7ebce5b" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="762" height="182" alt="image" src="https://github.com/user-attachments/assets/b1320329-8856-4bcc-998a-3e3d131ffd8f" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="835" height="113" alt="image" src="https://github.com/user-attachments/assets/45ad73bb-c0e4-4653-8acb-927206194970" />


seq 10 
## OUTPUT

<img width="779" height="273" alt="image" src="https://github.com/user-attachments/assets/93b418c2-1c55-49c5-bc10-15097679a1b4" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="942" height="122" alt="image" src="https://github.com/user-attachments/assets/2fe255d9-9865-4b65-9007-ce1d3a587fb6" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="764" height="117" alt="image" src="https://github.com/user-attachments/assets/fbbf06f8-17a8-444d-976c-85f3374c4543" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="679" height="139" alt="image" src="https://github.com/user-attachments/assets/2154fb16-a3d4-4d4a-b1be-12e8cbf5a8d2" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="623" height="110" alt="image" src="https://github.com/user-attachments/assets/2857ad9b-3c1d-483b-b1bc-c7f332bedc21" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="839" height="119" alt="image" src="https://github.com/user-attachments/assets/f1ae0409-9d97-47fe-9ee0-ef12a70a1319" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1003" height="112" alt="image" src="https://github.com/user-attachments/assets/d9efd312-73c4-4ab8-99ae-37e5a2f75f52" />


sed -n '2,4{s/$/*/;p}' file23

<img width="912" height="113" alt="image" src="https://github.com/user-attachments/assets/a73ffbe6-54ed-403c-99b0-6a27911d424c" />


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

<img width="732" height="516" alt="image" src="https://github.com/user-attachments/assets/5c306f70-da9b-4e1e-a855-2b2dc9df44b1" />

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

<img width="812" height="567" alt="image" src="https://github.com/user-attachments/assets/23bdc300-eb7a-4507-b889-dfe82e20813b" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="882" height="420" alt="image" src="https://github.com/user-attachments/assets/df0d3db5-b345-4498-a955-74284d353425" />

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

<img width="766" height="185" alt="image" src="https://github.com/user-attachments/assets/e276875b-e92e-4d08-ae88-b9b2fb3ec0a9" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="883" height="193" alt="image" src="https://github.com/user-attachments/assets/d738d303-bac4-49d8-8c4b-27918dec438e" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="926" height="632" alt="image" src="https://github.com/user-attachments/assets/fc65f6e5-0f94-4fd9-bc14-f564ad6abac1" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT



tar -xvf backup.tar
## OUTPUT
<img width="989" height="632" alt="image" src="https://github.com/user-attachments/assets/c6c0ab52-b783-48dd-8cbc-3ab0de77ece6" />

gzip backup.tar

ls .gz
## OUTPUT
 
 <img width="741" height="95" alt="image" src="https://github.com/user-attachments/assets/5ddf9bbb-f577-452d-a4c5-5d19e21d0468" />

gunzip backup.tar.gz
## OUTPUT

<img width="1169" height="118" alt="image" src="https://github.com/user-attachments/assets/f295faa1-436c-4a06-8425-d1ab1055790b" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="872" height="233" alt="image" src="https://github.com/user-attachments/assets/11cb246d-b19e-409c-b2eb-73851107796f" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="675" height="364" alt="image" src="https://github.com/user-attachments/assets/0e0ceb18-6243-4fef-adb1-8c108c1b0775" />

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

 <img width="948" height="66" alt="image" src="https://github.com/user-attachments/assets/fe48b793-3879-4ff9-b68a-c12994b5837f" />

ls file1
## OUTPUT

<img width="915" height="772" alt="image" src="https://github.com/user-attachments/assets/4f826eb3-9ab0-47e1-adc6-6c09a0038743" />

echo $?
## OUTPUT 
<img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/43895f65-cbee-4a54-90b3-40e434a68103" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
 <img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/35946707-d22b-4353-8059-b44cb7483ad9" />
abcd
 
echo $?
 ## OUTPUT

<img width="638" height="71" alt="image" src="https://github.com/user-attachments/assets/d597c576-f39b-44cc-aa1f-be63d36d2d75" />
 
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

<img width="1159" height="925" alt="image" src="https://github.com/user-attachments/assets/6436e8f6-8c60-4750-b38b-d7187692f440" />

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

<img width="1160" height="746" alt="image" src="https://github.com/user-attachments/assets/95325136-6a5b-4968-b59d-7389179f23da" />

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

<img width="1004" height="818" alt="image" src="https://github.com/user-attachments/assets/6eb8816c-6beb-48a6-bf69-e42bc0a1e004" />

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

<img width="1157" height="928" alt="image" src="https://github.com/user-attachments/assets/0a36d65f-f4bd-4edd-8ffb-b1c52b1de9b0" />
<img width="1149" height="930" alt="image" src="https://github.com/user-attachments/assets/52806164-d588-447e-a0ed-f9c6f4fabed3" />

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

<img width="1160" height="928" alt="image" src="https://github.com/user-attachments/assets/5fffcd73-4212-4978-9f4b-353beb9266f4" />


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

<img width="970" height="638" alt="image" src="https://github.com/user-attachments/assets/86e8c214-7871-4444-ab2f-464cd985a0e6" />

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
 
 <img width="895" height="411" alt="image" src="https://github.com/user-attachments/assets/a605ab36-a608-46de-86c9-31c2818b5d94" />

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
 
 <img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/ed49adf2-35a6-4dc8-b225-aae94ef6bb67" />

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
 
 <img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/852a699d-d5e9-4478-8eda-f658e5e01a1c" />
3
 
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
 
 <img width="771" height="812" alt="image" src="https://github.com/user-attachments/assets/d29690e2-79dd-4243-bcaf-ca826a3b1534" />

 
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
 
 <img width="700" height="311" alt="image" src="https://github.com/user-attachments/assets/df72e98a-d7d2-43a1-a800-a86fbf36d523" />

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
 
 <img width="625" height="431" alt="image" src="https://github.com/user-attachments/assets/732053ed-809d-4910-9520-3cdcfe193547" />

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
 
 <img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/6982edb4-1c6e-4da5-9163-66280a81c957" />

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

<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/b8eb8c59-2926-41fa-a2cf-8bbcc0e145fa" />

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

<img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/47f4276a-8343-40ca-8cd0-3527b5909118" />


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

<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/a5696932-7876-4367-9210-cf569c5afd65" />

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

<img width="768" height="503" alt="image" src="https://github.com/user-attachments/assets/164fc5a3-f879-473c-bf5e-ac8a45269cf8" />

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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
 <img width="731" height="362" alt="image" src="https://github.com/user-attachments/assets/260ae1b0-ee36-4633-aaf1-c70ac295a6fa" />

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
 
 <img width="658" height="386" alt="image" src="https://github.com/user-attachments/assets/0a1869af-cc92-4225-9ab9-757ae42f0e35" />

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

<img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/0b6ac7e8-6817-4ef4-899c-71d506b1e0a4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="440" height="226" alt="image" src="https://github.com/user-attachments/assets/2e654b19-ea12-4820-a652-51a73c271b64" />

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
 
 <img width="513" height="323" alt="image" src="https://github.com/user-attachments/assets/4c5f3c96-7a56-49ad-bd80-1e4f889f9332" />

 ./funcex.sh 


 
 ./funcex.sh 1 2

<img width="526" height="346" alt="image" src="https://github.com/user-attachments/assets/0e4f7887-de86-437d-a27b-5e402506dc37" />
 
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

<img width="593" height="486" alt="image" src="https://github.com/user-attachments/assets/0dc908b5-4be9-449d-8bf3-731016597ad1" />

$ ./argshift.sh 1 2 3
 
 <img width="569" height="322" alt="image" src="https://github.com/user-attachments/assets/21566e6d-9d5a-43f0-b5e0-0f01c482e78e" />
 
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

<img width="563" height="452" alt="image" src="https://github.com/user-attachments/assets/aad38965-7107-415d-9a07-5574709adab3" />

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
 
 <img width="563" height="452" alt="image" src="https://github.com/user-attachments/assets/d0c69f34-7a6c-4669-8514-7087c61d2539" />
 
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
 
 <img width="510" height="755" alt="image" src="https://github.com/user-attachments/assets/a6fbda02-9a86-4af7-bee0-d62a50bb4eba" />

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

<img width="581" height="541" alt="image" src="https://github.com/user-attachments/assets/c209fc4b-ab32-4901-946a-0e21012037a8" />

# RESULT:
The Commands are executed successfully.
