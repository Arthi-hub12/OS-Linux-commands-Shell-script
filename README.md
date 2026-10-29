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

<img width="627" height="177" alt="Screenshot 2026-10-29 120515" src="https://github.com/user-attachments/assets/fced136e-5d86-4a8f-8df4-b074887034e8" />


cat < file2
## OUTPUT
<img width="650" height="198" alt="Screenshot 2026-10-29 120524" src="https://github.com/user-attachments/assets/7d434cce-c964-47f1-8af3-fdf5b3d8dc8e" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="571" height="81" alt="Screenshot 2026-10-29 120534" src="https://github.com/user-attachments/assets/16373860-3c38-4ddb-a192-3ae0e9daa5fa" />

comm file1 file2
 ## OUTPUT
<img width="576" height="197" alt="Screenshot 2026-10-29 120542" src="https://github.com/user-attachments/assets/e296ef12-ec56-4f79-9ff8-ecf2c6b2f2a4" />

 
diff file1 file2
## OUTPUT
<img width="663" height="315" alt="Screenshot 2026-10-29 120552" src="https://github.com/user-attachments/assets/66b868fd-6ba5-41b1-ad97-f11207107419" />


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


<img width="617" height="123" alt="Screenshot 2026-10-29 120606" src="https://github.com/user-attachments/assets/517f9b84-2166-471a-8fed-d8e3d1a56d24" />


cut -d "|" -f 1 file22
## OUTPUT


<img width="647" height="127" alt="Screenshot 2026-10-29 120619" src="https://github.com/user-attachments/assets/02d4e9cd-6d8b-42d7-9d60-79b9c1018d16" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="626" height="132" alt="Screenshot 2026-10-29 120628" src="https://github.com/user-attachments/assets/c05a2826-9264-473b-8e6f-23de08f464c0" />


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
<img width="568" height="77" alt="Screenshot 2026-10-29 120640" src="https://github.com/user-attachments/assets/3b6e85b6-3d27-4b00-ba99-b80162069c0e" />



grep hello newfile 
## OUTPUT


<img width="567" height="85" alt="Screenshot 2026-10-29 120653" src="https://github.com/user-attachments/assets/0855da81-32a8-41dd-ad85-982ea1169a86" />


grep -v hello newfile 
## OUTPUT

<img width="567" height="85" alt="Screenshot 2026-10-29 120653" src="https://github.com/user-attachments/assets/0efdf63d-045c-4607-abe3-28897411bc29" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="520" height="106" alt="Screenshot 2026-10-29 120930" src="https://github.com/user-attachments/assets/c6ea5d2b-49f1-4f70-bb6b-65de2ba756ae" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="552" height="71" alt="Screenshot 2026-10-29 120715" src="https://github.com/user-attachments/assets/a7a8b36e-c3eb-454c-967e-b7d819f4f520" />


grep -R ubuntu /etc
## OUTPUT
<img width="571" height="83" alt="Screenshot 2026-10-29 120722" src="https://github.com/user-attachments/assets/a1ce753e-fef1-4702-abd7-acfe3158a9b1" />



grep -w -n world newfile   
## OUTPUT

<img width="546" height="73" alt="Screenshot 2026-10-29 120840" src="https://github.com/user-attachments/assets/f7a4bfa3-398f-42c7-903f-74eb18cfe827" />

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


<img width="530" height="71" alt="Screenshot 2026-10-29 120923" src="https://github.com/user-attachments/assets/81794349-7b81-4d46-bba9-d2c26115e3ed" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="550" height="93" alt="Screenshot 2026-10-29 120856" src="https://github.com/user-attachments/assets/056e4005-86a9-44df-993b-eb5ffd691460" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



<img width="1600" height="769" alt="WhatsApp Image 2026-10-24 at 9 11 10 PM" src="https://github.com/user-attachments/assets/8307642f-3538-4005-bca4-1c69bbb80527" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="587" height="122" alt="Screenshot 2026-10-29 120939" src="https://github.com/user-attachments/assets/4052263f-dd32-4864-8c61-4cad5321c68f" />


egrep '(world$)' newfile 
## OUTPUT

<img width="562" height="77" alt="Screenshot 2026-10-29 120910" src="https://github.com/user-attachments/assets/784e4a11-a79e-4ca5-9adf-3568a3d0bf58" />


egrep '(World$)' newfile 
## OUTPUT

<img width="800" height="601" alt="Screenshot 2026-10-29 120735" src="https://github.com/user-attachments/assets/0db67297-98ae-4a17-8ae2-995cadabfb23" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="533" height="98" alt="Screenshot 2026-10-29 120818" src="https://github.com/user-attachments/assets/bc5aa31f-b0b3-45ed-893f-8539741d03e6" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="571" height="81" alt="Screenshot 2026-10-29 120534" src="https://github.com/user-attachments/assets/99506766-5630-4f64-b70f-30e297879a1a" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="517" height="72" alt="Screenshot 2026-10-29 120917" src="https://github.com/user-attachments/assets/d7bc7bae-0aec-4e82-8b90-b4d9f28bb72f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="540" height="95" alt="Screenshot 2026-10-29 120848" src="https://github.com/user-attachments/assets/3f0312fe-9401-49fb-989e-40e473b83d8e" />


egrep l{2} newfile
## OUTPUT

<img width="626" height="132" alt="Screenshot 2026-10-29 120628" src="https://github.com/user-attachments/assets/860144fb-772d-4081-8d68-9e4f931ee102" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="561" height="105" alt="Screenshot 2026-10-29 120743" src="https://github.com/user-attachments/assets/fa5deff0-f2d4-4557-bb42-a17507cfa91a" />


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


<img width="613" height="126" alt="Screenshot 2026-10-29 120904" src="https://github.com/user-attachments/assets/9feee99a-4d8e-49ce-8b0b-8832686fcd5e" />

sed -n -e '$p' file23
## OUTPUT

<img width="571" height="83" alt="Screenshot 2026-10-29 120722" src="https://github.com/user-attachments/assets/03ea50a4-75ab-4a33-8afa-ca8dc02a6292" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="617" height="123" alt="Screenshot 2026-10-29 120606" src="https://github.com/user-attachments/assets/135243f5-5328-4dbd-9a8e-0743420396aa" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="562" height="77" alt="Screenshot 2026-10-29 120910" src="https://github.com/user-attachments/assets/a05335a3-a498-4e3c-8ec1-fc1b907864de" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="517" height="72" alt="Screenshot 2026-10-29 120917" src="https://github.com/user-attachments/assets/c70bdb47-7cdc-4e5a-86f2-f3b6eeed559c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="550" height="93" alt="Screenshot 2026-10-29 120856" src="https://github.com/user-attachments/assets/53a8ace6-dccc-4fc3-9272-8ae3f29be7c0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="520" height="106" alt="Screenshot 2026-10-29 120930" src="https://github.com/user-attachments/assets/28ef58dc-125c-4baf-9c99-526127ec8f98" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="613" height="126" alt="Screenshot 2026-10-29 120904" src="https://github.com/user-attachments/assets/dc032c03-b6bc-4fe7-9aae-d83fc54be6d2" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="568" height="77" alt="Screenshot 2026-10-29 120640" src="https://github.com/user-attachments/assets/7057f526-129f-40fd-b933-f36ef8e8a669" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="613" height="126" alt="Screenshot 2026-10-29 120904" src="https://github.com/user-attachments/assets/3d059baa-a148-40ea-959a-e2421a7bf6ac" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="587" height="122" alt="Screenshot 2026-10-29 120939" src="https://github.com/user-attachments/assets/1e41edf0-45dc-4258-92e5-09f66ab55ed6" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="552" height="71" alt="Screenshot 2026-10-29 120715" src="https://github.com/user-attachments/assets/34f6d0bc-3ff3-4030-a627-ae8ee398f51f" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="520" height="106" alt="Screenshot 2026-10-29 120930" src="https://github.com/user-attachments/assets/007e1f64-f920-4990-8756-d35dad1f1ac1" />

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
<img width="546" height="73" alt="Screenshot 2026-10-29 120840" src="https://github.com/user-attachments/assets/adea30d0-4f2f-453b-90de-92e745b00c9b" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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

<img width="550" height="93" alt="Screenshot 2026-10-29 120856" src="https://github.com/user-attachments/assets/b6739027-1157-4de5-a5bf-90e655060eeb" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="626" height="132" alt="Screenshot 2026-10-29 120628" src="https://github.com/user-attachments/assets/35840869-133d-4da9-a95b-e022fe53f6a7" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

<img width="530" height="71" alt="Screenshot 2026-10-29 120923" src="https://github.com/user-attachments/assets/09c2b3f0-9e60-42d1-afc2-3004ba6c4d10" />

gunzip backup.tar.gz
## OUTPUT
<img width="550" height="93" alt="Screenshot 2026-10-29 120856" src="https://github.com/user-attachments/assets/7d1103e3-7b8d-4fd6-b419-3d0236adc922" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="650" height="198" alt="Screenshot 2026-10-29 120524" src="https://github.com/user-attachments/assets/50b92d76-bb03-4c82-9c26-b0bb6065e303" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="566" height="88" alt="Screenshot 2026-10-29 120831" src="https://github.com/user-attachments/assets/4cef92d2-69a0-433a-a9f5-a54024a6535a" />

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
<img width="517" height="72" alt="Screenshot 2026-10-29 120917" src="https://github.com/user-attachments/assets/e72b9e50-219a-4f02-9c3c-d7841e0f5631" />

 
ls file1
## OUTPUT
<img width="552" height="71" alt="Screenshot 2026-10-29 120715" src="https://github.com/user-attachments/assets/c5017625-5e3f-428b-8db0-a4041da4d966" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="571" height="72" alt="Screenshot 2026-10-29 120702" src="https://github.com/user-attachments/assets/1430ee0b-9005-4e2c-9e41-5ef4a56672db" />

abcd
 
echo $?
 ## OUTPUT

<img width="1600" height="769" alt="WhatsApp Image 2026-10-24 at 9 11 43 PM" src="https://github.com/user-attachments/assets/cfcca801-1dc5-4e4e-b8db-b2d1120c5221" />

 
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



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 




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


# RESULT:
The Commands are executed successfully.
