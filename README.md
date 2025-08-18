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

<img width="318" height="150" alt="image" src="https://github.com/user-attachments/assets/56212b17-9714-42b7-b71d-75779949409f" />


cat < file2
## OUTPUT
<img width="407" height="172" alt="image" src="https://github.com/user-attachments/assets/b0469752-3d16-4768-a752-224c722aaf90" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="432" height="78" alt="image" src="https://github.com/user-attachments/assets/73a8c45b-7062-47b7-b9a3-9be9ae3980ff" />

comm file1 file2
 ## OUTPUT
<img width="447" height="228" alt="image" src="https://github.com/user-attachments/assets/3921c2f5-eacf-44f4-809f-764ed35d901e" />

 
diff file1 file2
## OUTPUT
<img width="461" height="277" alt="image" src="https://github.com/user-attachments/assets/3ec1eed4-0c5b-44ef-99b3-44689c19196a" />


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

<img width="378" height="93" alt="image" src="https://github.com/user-attachments/assets/b5f6f2bf-fb9a-4719-8c6f-a059deb5c0d5" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="380" height="117" alt="image" src="https://github.com/user-attachments/assets/9ae193ca-a171-45cd-8453-2b7fcad95d37" />


cut -d "|" -f 2 file22
## OUTPUT
c<img width="468" height="136" alt="image" src="https://github.com/user-attachments/assets/dee92d6d-e221-40f4-871b-d1589a096f13" />


cat < newfile 
```
Hello world
hello world
^d
````
<img width="395" height="111" alt="image" src="https://github.com/user-attachments/assets/8d6a9216-a6e9-426f-955f-d692721e974b" />

cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="371" height="71" alt="image" src="https://github.com/user-attachments/assets/b072c923-ecc9-40d9-b25d-1a181f88ae4d" />



grep hello newfile 
## OUTPUT
<img width="381" height="82" alt="image" src="https://github.com/user-attachments/assets/8da9f9c3-0cfa-445e-bf13-ab3b1c6722f6" />




grep -v hello newfile 
## OUTPUT

<img width="370" height="72" alt="image" src="https://github.com/user-attachments/assets/268a5a76-833e-4829-80b7-c1f79d6625fb" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="477" height="103" alt="image" src="https://github.com/user-attachments/assets/9a944a71-0239-4a44-8725-2ecceeb688b9" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="452" height="78" alt="image" src="https://github.com/user-attachments/assets/4cd60fd2-c1bb-4c2c-884b-9094352e39e5" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="422" height="102" alt="image" src="https://github.com/user-attachments/assets/5b5da692-1a76-4930-bdc6-b9a232ea35d4" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
<img width="585" height="131" alt="image" src="https://github.com/user-attachments/assets/2bf31c46-93be-4600-8c11-8b03946cd170" />

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
<img width="441" height="85" alt="image" src="https://github.com/user-attachments/assets/ba36e358-7a04-499a-a752-3363e4d608c1" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="438" height="113" alt="image" src="https://github.com/user-attachments/assets/ba4a8eb8-084d-4e01-bab0-8cb7ca35210b" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="527" height="97" alt="image" src="https://github.com/user-attachments/assets/d667dac2-480c-4b03-977f-5ec44de34e21" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="438" height="101" alt="image" src="https://github.com/user-attachments/assets/028ac979-60a2-4612-80bb-77f17745268e" />


egrep '(world$)' newfile 
## OUTPUT

<img width="386" height="110" alt="image" src="https://github.com/user-attachments/assets/9b9eaa46-1e31-43bf-9cb2-537df1646b20" />


egrep '(World$)' newfile 
## OUTPUT
<img width="372" height="81" alt="image" src="https://github.com/user-attachments/assets/f47f68e0-6e56-4686-8852-a16fc4840c25" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="426" height="136" alt="image" src="https://github.com/user-attachments/assets/af3d8dc0-2330-421e-b084-ae383fd9d53e" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="337" height="83" alt="image" src="https://github.com/user-attachments/assets/34b65bfd-353a-4851-993d-9b2809600401" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="441" height="76" alt="image" src="https://github.com/user-attachments/assets/e1e682a3-5071-48c8-9d48-bca4cf9b41cd" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="452" height="87" alt="image" src="https://github.com/user-attachments/assets/c5f2b661-5902-461d-a1eb-5810e6268963" />


egrep l{2} newfile
## OUTPUT

<img width="446" height="102" alt="image" src="https://github.com/user-attachments/assets/5e1a09f1-d79f-4112-9051-b413de6d819b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="431" height="132" alt="image" src="https://github.com/user-attachments/assets/2b194e15-16dd-4c10-98e6-65e677d6b90f" />


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
<img width="485" height="72" alt="image" src="https://github.com/user-attachments/assets/be1ac089-8f5a-499c-b665-d8232d24a7f8" />



sed -n -e '$p' file23
## OUTPUT
<img width="318" height="82" alt="image" src="https://github.com/user-attachments/assets/0c92a4e3-a944-40b1-8ced-68ae5450bbdc" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="537" height="231" alt="image" src="https://github.com/user-attachments/assets/4dd535ab-1f50-4750-a2e6-199e8d9de2ed" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="543" height="232" alt="image" src="https://github.com/user-attachments/assets/e6a4ee59-c5cf-4bf4-bc64-d611e65aab05" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="602" height="233" alt="image" src="https://github.com/user-attachments/assets/602806a0-aa2b-47d6-8d43-2c8b32d9ff9b" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="437" height="170" alt="image" src="https://github.com/user-attachments/assets/83b7e018-1b53-4d8f-affd-823b2d29d6b2" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="427" height="125" alt="image" src="https://github.com/user-attachments/assets/a8460fc8-ac7e-43dc-8846-5ef30a09e9ef" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="462" height="106" alt="image" src="https://github.com/user-attachments/assets/73c032e0-0345-49dc-81b9-bf94acc8bdc8" />


seq 10 
## OUTPUT
<img width="403" height="292" alt="image" src="https://github.com/user-attachments/assets/b85517c1-7d3e-42e4-a8a4-e5689cd81066" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="340" height="145" alt="image" src="https://github.com/user-attachments/assets/657567f4-0fc3-442b-b224-9f5c430644bf" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="381" height="143" alt="image" src="https://github.com/user-attachments/assets/7a6f4339-d92d-43d9-9183-b0ba946401b7" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/4b89648d-0a5e-4028-97ec-628c56629c90" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="425" height="132" alt="image" src="https://github.com/user-attachments/assets/acc98f58-8d7c-4c3f-a85a-a59945801a22" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="410" height="133" alt="image" src="https://github.com/user-attachments/assets/0f926c39-3e00-4319-9f85-a2716dcbf875" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="540" height="125" alt="image" src="https://github.com/user-attachments/assets/9c02a1b1-d473-4fa0-8821-f390ad86e619" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="462" height="127" alt="image" src="https://github.com/user-attachments/assets/0312d1a9-13d5-4387-99c0-baa953d6f89c" />



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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



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

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
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
