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

<img width="485" height="95" alt="image" src="https://github.com/user-attachments/assets/92cc6497-7138-44a4-9b61-caf41906ee37" />




cat < file2
## OUTPUT

<img width="487" height="107" alt="image" src="https://github.com/user-attachments/assets/e6c685d1-8323-4728-867f-6aed95a82727" />



# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="361" height="32" alt="image" src="https://github.com/user-attachments/assets/4e83b1aa-15ba-4fa2-acef-1d8ef348c32a" />


comm file1 file2
 ## OUTPUT
 
<img width="386" height="167" alt="image" src="https://github.com/user-attachments/assets/7ddedd7b-d66f-4114-9636-988e9c18b1cb" />


 
diff file1 file2
## OUTPUT
<img width="401" height="180" alt="image" src="https://github.com/user-attachments/assets/23c307c0-fedd-47ad-9707-4d15fbacffc2" />





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

<img width="333" height="62" alt="image" src="https://github.com/user-attachments/assets/99be0642-8027-4f8a-853d-7384e5189609" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="407" height="82" alt="image" src="https://github.com/user-attachments/assets/4505148b-fe1a-4192-97c5-86ddbf5f8a26" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="352" height="80" alt="image" src="https://github.com/user-attachments/assets/91063a81-4bf5-4966-8643-42b4a48a6be6" />


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

<img width="290" height="42" alt="image" src="https://github.com/user-attachments/assets/8d0bdd90-e184-4418-8ece-44b10fa75fb2" />


grep hello newfile 
## OUTPUT

<img width="327" height="50" alt="image" src="https://github.com/user-attachments/assets/b83866d3-4736-4bb5-9d35-0f34eb101c0b" />



grep -v hello newfile 
## OUTPUT
<img width="372" height="38" alt="image" src="https://github.com/user-attachments/assets/2dfe8599-b345-4fb5-9ca8-8e5deee38116" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="435" height="65" alt="image" src="https://github.com/user-attachments/assets/2d91241d-1af3-448c-b22b-6d80befd2c29" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="480" height="46" alt="image" src="https://github.com/user-attachments/assets/b434da67-dd1b-47f6-8c1d-2137090a6ea2" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="365" height="75" alt="image" src="https://github.com/user-attachments/assets/4817a62c-93e1-4e6e-88c6-d9148d646de8" />


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

<img width="410" height="60" alt="image" src="https://github.com/user-attachments/assets/79f478a3-fd7c-4300-8b65-3ace57033cf4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="427" height="62" alt="image" src="https://github.com/user-attachments/assets/e6ab4e6d-ea28-4271-935b-2a74d363a2be" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="447" height="63" alt="image" src="https://github.com/user-attachments/assets/6b95437e-6639-4bd8-aae0-2c728e0d6701" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="427" height="47" alt="image" src="https://github.com/user-attachments/assets/f356cb53-2e2d-43d4-bf3a-42ee62def1b2" />


egrep '(world$)' newfile 
## OUTPUT


<img width="420" height="71" alt="image" src="https://github.com/user-attachments/assets/b8c964ef-1dd9-43e8-b16f-9182a4d4fd07" />


egrep '(World$)' newfile 
## OUTPUT

<img width="327" height="47" alt="image" src="https://github.com/user-attachments/assets/338afd62-3d01-4e03-9f4e-2cc5988e5266" />
egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="357" height="76" alt="image" src="https://github.com/user-attachments/assets/61d75ba3-e618-44d9-af37-6d4c51e30820" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="365" height="47" alt="image" src="https://github.com/user-attachments/assets/627127c1-c876-4636-8b6e-88d96a66bb59" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="348" height="47" alt="image" src="https://github.com/user-attachments/assets/5b8e9e92-8e71-44d2-850c-5bde49f4943b" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="342" height="45" alt="image" src="https://github.com/user-attachments/assets/2c6cd17c-6774-43d8-ba82-5420339fb8d7" />

egrep l{2} newfile
## OUTPUT

<img width="643" height="61" alt="image" src="https://github.com/user-attachments/assets/0dbd5d5f-6631-4655-9212-2d37953e82d3" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="407" height="77" alt="image" src="https://github.com/user-attachments/assets/e0aa1287-ea45-4d5d-9028-6d94d4fb9987" />

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

<img width="343" height="47" alt="image" src="https://github.com/user-attachments/assets/ed090b23-f9e5-43a9-9902-5390fb7c6907" />


sed -n -e '$p' file23
## OUTPUT
<img width="381" height="45" alt="image" src="https://github.com/user-attachments/assets/dc790ee9-3e4e-4125-9dbc-ecca82148a47" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="433" height="150" alt="image" src="https://github.com/user-attachments/assets/4e676d6b-780a-4059-8a5d-d059fc051f1d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="452" height="151" alt="image" src="https://github.com/user-attachments/assets/44c66e46-93fe-4854-8edf-a643f95c72e7" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="611" height="151" alt="image" src="https://github.com/user-attachments/assets/d8a94641-61e3-49ca-8c7a-f22aa9d0b9fd" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="542" height="105" alt="image" src="https://github.com/user-attachments/assets/8c52491e-d491-44b2-9243-8a68284ad209" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="560" height="77" alt="image" src="https://github.com/user-attachments/assets/a27200ae-1795-4703-98c9-8c712e667242" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="598" height="65" alt="image" src="https://github.com/user-attachments/assets/d62b015f-cb17-4219-87d4-83e529ac1130" />


seq 10 
## OUTPUT

<img width="678" height="178" alt="image" src="https://github.com/user-attachments/assets/3d0be5f3-3532-499d-93db-aa7cd923adf9" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="406" height="72" alt="image" src="https://github.com/user-attachments/assets/769e400f-2d59-4907-9688-938d535613a0" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="477" height="81" alt="image" src="https://github.com/user-attachments/assets/f2771d8e-9715-4adb-9777-929c667455f4" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="363" height="92" alt="image" src="https://github.com/user-attachments/assets/ee7f7816-2ff9-4fc1-9fdd-66e0211b214d" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="352" height="77" alt="image" src="https://github.com/user-attachments/assets/dbae3581-d3ce-41f4-96be-9e77bdb5210f" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="447" height="78" alt="image" src="https://github.com/user-attachments/assets/381bddc9-ae26-4ff5-86a5-45114f4d3558" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="377" height="72" alt="image" src="https://github.com/user-attachments/assets/92dd1f75-284c-427a-8156-62220a6bf5a8" />



sed -n '2,4{s/$/*/;p}' file23
<img width="437" height="76" alt="image" src="https://github.com/user-attachments/assets/380ddf0e-ab82-4637-b931-ea1af4420906" />


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

<img width="320" height="106" alt="image" src="https://github.com/user-attachments/assets/cd82d57e-425a-4836-9483-29b3bfda7c29" />

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

<img width="478" height="110" alt="image" src="https://github.com/user-attachments/assets/3e5a913d-eb24-42da-9988-572e7f56150d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="448" height="147" alt="image" src="https://github.com/user-attachments/assets/88fbf7c2-cfc2-47c2-9d71-c8fe06945288" />

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

<img width="363" height="77" alt="image" src="https://github.com/user-attachments/assets/bc303546-14a9-4f24-b986-685430c859e5" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="495" height="75" alt="image" src="https://github.com/user-attachments/assets/4c919063-70ac-48f0-ab11-56187d6a391e" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="758" height="166" alt="image" src="https://github.com/user-attachments/assets/cdaa9470-9043-400f-aa63-c386a00e513b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="863" height="162" alt="image" src="https://github.com/user-attachments/assets/13e6a425-3a14-4014-987f-8b152b67a988" />

tar -xvf backup.tar
## OUTPUT
<img width="815" height="167" alt="image" src="https://github.com/user-attachments/assets/d6774571-edc0-4017-916a-00692fbe2e95" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="493" height="60" alt="image" src="https://github.com/user-attachments/assets/a64bcc36-43e8-4cd0-a3f3-e350370e70f6" />

gunzip backup.tar.gz
## OUTPUT

 
 <img width="731" height="37" alt="image" src="https://github.com/user-attachments/assets/0c900852-29c7-48cd-bcc5-813d4ff4036c" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="327" height="65" alt="image" src="https://github.com/user-attachments/assets/d9b50031-9f9c-4afd-8097-f44e7678f51f" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="427" height="78" alt="image" src="https://github.com/user-attachments/assets/21195948-29ca-4501-8744-7274f1daf5bf" />

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

 <img width="862" height="273" alt="image" src="https://github.com/user-attachments/assets/55b8f5d1-408e-4a48-baa4-f2e35ea91133" />

ls file1
## OUTPUT
<img width="418" height="51" alt="image" src="https://github.com/user-attachments/assets/8a37b877-e7bd-48f7-a221-2e465acbe62e" />

echo $?
## OUTPUT 
<img width="415" height="41" alt="image" src="https://github.com/user-attachments/assets/06a23eb8-7101-4420-9ed2-9e10a59ceafa" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="645" height="97" alt="image" src="https://github.com/user-attachments/assets/18bbc426-1a96-4177-bf46-e808e1a27fa4" />

abcd
 
echo $?
 ## OUTPUT


<img width="417" height="40" alt="image" src="https://github.com/user-attachments/assets/57211b4c-582c-4cd5-b7ee-b8d3e79ef123" />

 
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
<img width="530" height="165" alt="image" src="https://github.com/user-attachments/assets/d2e76cd7-8522-474d-b8ce-934aafe6e19c" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="380" height="28" alt="image" src="https://github.com/user-attachments/assets/a2eac99f-0921-422b-a326-bbfd0e04c207" />

<img width="608" height="62" alt="image" src="https://github.com/user-attachments/assets/6e82ac55-a544-43d5-97b0-23d9846ecf5a" />

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
<img width="590" height="65" alt="image" src="https://github.com/user-attachments/assets/adc4ea74-c2c1-41c8-81b4-2d2612101996" />

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

<img width="613" height="78" alt="image" src="https://github.com/user-attachments/assets/6730f415-31cd-4972-9669-03158794b422" />


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
<img width="587" height="118" alt="image" src="https://github.com/user-attachments/assets/7f848345-11e2-4331-9c2d-8947e93a8757" />

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

<img width="500" height="122" alt="image" src="https://github.com/user-attachments/assets/5d8fda03-a7fe-4649-9734-2ae42a90e77e" />

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

<img width="322" height="105" alt="image" src="https://github.com/user-attachments/assets/015ee297-0f29-447b-9b92-990e507db7cc" />


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
<img width="522" height="90" alt="image" src="https://github.com/user-attachments/assets/509682d2-be13-42d9-9b2a-ae99d2d36468" />

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
## OUTPUT:
<img width="358" height="42" alt="image" src="https://github.com/user-attachments/assets/e2a8d0ad-1c78-4990-a30f-a5ef18581652" />

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
 ## Output:
 <img width="496" height="182" alt="image" src="https://github.com/user-attachments/assets/bda8a269-97c9-46a8-9b48-b396f5b1a731" />

 
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
 
 ## Output:
 <img width="490" height="110" alt="image" src="https://github.com/user-attachments/assets/71305dcd-095c-4204-9184-af034d4cf3c8" />

 
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
 ## Output:
 <img width="517" height="152" alt="image" src="https://github.com/user-attachments/assets/ccd6e9a6-67d1-4cce-9ffc-fd924c5ed32a" />

 
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
 ## Output:
 <img width="535" height="107" alt="image" src="https://github.com/user-attachments/assets/d4156612-74c1-4760-9067-a5600b81fbdf" />

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
 ## output
 <img width="900" height="297" alt="image" src="https://github.com/user-attachments/assets/e625f893-7701-4589-8822-481124761371" />


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
<img width="900" height="462" alt="image" src="https://github.com/user-attachments/assets/0dc9ff53-de2d-42db-9fb6-12c642c77bbd" />

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
<img width="315" height="107" alt="image" src="https://github.com/user-attachments/assets/e4f734fa-2bea-4838-967e-fa35271f0c59" />

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
<img width="282" height="208" alt="image" src="https://github.com/user-attachments/assets/5c0fbc2b-8a31-4ca9-a2f7-57a5b86c315e" />

 
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
<img width="576" height="87" alt="image" src="https://github.com/user-attachments/assets/ce8026cd-d111-41eb-b42d-5ca7e094c318" />

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


# RESULT:
The Commands are executed successfully.
