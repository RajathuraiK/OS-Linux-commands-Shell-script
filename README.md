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

<img width="1322" height="433" alt="image" src="https://github.com/user-attachments/assets/18eb2f1b-e88e-4852-9798-a3245896d941" />


cat < file2
## OUTPUT

<img width="1320" height="507" alt="image" src="https://github.com/user-attachments/assets/14b06911-7dc1-409f-97cc-54c8ba7a4421" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="1300" height="223" alt="Screenshot 2026-06-03 185550" src="https://github.com/user-attachments/assets/dd8b33de-f7da-4529-9373-34012c53ba63" />

comm file1 file2
 ## OUTPUT

<img width="1378" height="671" alt="image" src="https://github.com/user-attachments/assets/02dd9a92-cb80-4318-8105-30155f8a5e67" />

 
diff file1 file2
## OUTPUT

<img width="1210" height="772" alt="image" src="https://github.com/user-attachments/assets/0d97feb0-a3dd-4756-add4-fb9be2224fba" />

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

<img width="1075" height="290" alt="image" src="https://github.com/user-attachments/assets/fb50de96-9572-477b-ab05-56386b9aecaa" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="1295" height="361" alt="image" src="https://github.com/user-attachments/assets/4407a3cc-3f81-4fd1-878f-dfe46a4c5098" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="1172" height="357" alt="image" src="https://github.com/user-attachments/assets/a37ccb53-84da-4832-8135-db9d9599b845" />

cat > newfile 
```
Hello world
hello world
^d
````

 
grep Hello newfile 
## OUTPUT

<img width="1169" height="233" alt="image" src="https://github.com/user-attachments/assets/049389ac-3537-483f-8747-1a45aeeb61f8" />


grep hello newfile 
## OUTPUT

<img width="1265" height="219" alt="image" src="https://github.com/user-attachments/assets/76acc938-a61b-4365-a2be-42e95a1be313" />


grep -v hello newfile 
## OUTPUT

<img width="1200" height="222" alt="image" src="https://github.com/user-attachments/assets/4f9aba37-26f9-468b-82ee-be33ab802e8a" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1415" height="295" alt="image" src="https://github.com/user-attachments/assets/1b8a072e-37a1-489f-8070-19e0a9aa8166" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1414" height="228" alt="image" src="https://github.com/user-attachments/assets/35a50c96-c738-4dcf-8da1-956e95ee5fa6" />


grep -R ubuntu /etc
## OUTPUT

<img width="1672" height="894" alt="image" src="https://github.com/user-attachments/assets/7576aa8d-884e-46b9-8789-01e169166441" />

<img width="1367" height="882" alt="image" src="https://github.com/user-attachments/assets/9c8b73db-33ea-4a96-a195-21da9ff95f70" />

grep -w -n world newfile   
## OUTPUT

<img width="937" height="182" alt="image" src="https://github.com/user-attachments/assets/9128dbd2-ee75-4729-8b42-c5dd648e76be" />


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

<img width="945" height="171" alt="image" src="https://github.com/user-attachments/assets/fe22f7c2-8cf8-44be-aaed-cc5c688e3f8c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="899" height="183" alt="image" src="https://github.com/user-attachments/assets/dfbac50c-c637-4b86-b65f-9fc1d617f6f5" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="902" height="171" alt="image" src="https://github.com/user-attachments/assets/7b6dfdfb-5bc4-4143-88cf-e0e1109966ae" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="867" height="135" alt="image" src="https://github.com/user-attachments/assets/d58ae429-b3c0-42fc-9546-858fd4f654eb" />


egrep '(world$)' newfile 
## OUTPUT

<img width="955" height="165" alt="image" src="https://github.com/user-attachments/assets/46ada36f-ca09-495e-96f0-c0356b81a654" />


egrep '(World$)' newfile 
## OUTPUT

<img width="752" height="131" alt="image" src="https://github.com/user-attachments/assets/ca6f7fc8-ed0f-4f4b-8f00-ffd520f1ef76" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="958" height="209" alt="image" src="https://github.com/user-attachments/assets/12298d8f-35eb-4296-b8bc-3b309675e569" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="896" height="132" alt="image" src="https://github.com/user-attachments/assets/9e24d1a1-8be0-4e0e-bd15-48089995b435" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="892" height="142" alt="image" src="https://github.com/user-attachments/assets/1b7dc20e-2a56-4380-9b26-8d1c9cbbd7e5" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="902" height="123" alt="image" src="https://github.com/user-attachments/assets/f8b97f33-7f3d-4fa0-aa52-a33cbcbacbef" />


egrep l{2} newfile
## OUTPUT

<img width="823" height="173" alt="image" src="https://github.com/user-attachments/assets/bf55ead3-f29d-49a4-b560-19d8e187b6d8" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1025" height="223" alt="image" src="https://github.com/user-attachments/assets/c5543045-973b-46ba-aaa1-1ad357e4735e" />


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

<img width="1087" height="179" alt="image" src="https://github.com/user-attachments/assets/53366f89-a577-461a-a953-906542106caa" />


sed -n -e '$p' file23
## OUTPUT

<img width="1070" height="189" alt="image" src="https://github.com/user-attachments/assets/a626e471-439a-49a0-93d8-056332d31ed6" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1154" height="611" alt="image" src="https://github.com/user-attachments/assets/7549cf77-51c5-4b2d-b8db-c1ab638b7d86" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1084" height="606" alt="image" src="https://github.com/user-attachments/assets/3b0172c8-8c4e-460f-b48e-d4b7afd172b3" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1117" height="605" alt="image" src="https://github.com/user-attachments/assets/9eed2e87-bae2-494f-9ad1-b1ec05bc27c4" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1118" height="420" alt="image" src="https://github.com/user-attachments/assets/69a7f4de-4e3c-4024-8373-04d95db860c1" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1423" height="315" alt="image" src="https://github.com/user-attachments/assets/4b740b9f-5052-4c50-9d75-84532c3dc529" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1170" height="245" alt="image" src="https://github.com/user-attachments/assets/27d06a44-2151-4fc1-9700-f681da9b7847" />


seq 10 
## OUTPUT

<img width="1078" height="707" alt="image" src="https://github.com/user-attachments/assets/20aef02e-b2e3-476c-8c69-b4936ded01fa" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="916" height="299" alt="image" src="https://github.com/user-attachments/assets/00ec5203-77ab-4d1e-875d-6f3ab7b56768" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1151" height="300" alt="image" src="https://github.com/user-attachments/assets/a995d849-a2dd-4351-a017-41074b1981c5" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="972" height="356" alt="image" src="https://github.com/user-attachments/assets/678db52e-ab0c-4df0-8cab-a8514a751413" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="1039" height="311" alt="image" src="https://github.com/user-attachments/assets/619e6be4-28ce-452c-95d2-c4f0e9e90dcb" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="904" height="299" alt="image" src="https://github.com/user-attachments/assets/efbb209a-b6b3-4d67-928b-5db2c4cf8abd" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1509" height="316" alt="image" src="https://github.com/user-attachments/assets/a0e57346-6357-421e-805d-4004dcb4d78f" />

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

<img width="1107" height="431" alt="image" src="https://github.com/user-attachments/assets/0aea7e15-a0a8-4b2b-a325-8b37f7a9f93f" />


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

<img width="1090" height="423" alt="image" src="https://github.com/user-attachments/assets/cd2fceb4-80d4-48fb-911c-d6f4258e3a75" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="1363" height="601" alt="image" src="https://github.com/user-attachments/assets/2aa1452e-fd67-4b99-9f84-568aeeddd36e" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```

cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="1121" height="302" alt="image" src="https://github.com/user-attachments/assets/c7836bf5-2ce2-458a-8386-20786214f1c9" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1545" height="296" alt="image" src="https://github.com/user-attachments/assets/727aaf45-6d0b-4abf-be7c-3b24dc8078ed" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1327" height="767" alt="image" src="https://github.com/user-attachments/assets/1ff540e6-b718-4f1b-b55b-4d374dfc059a" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1659" height="779" alt="image" src="https://github.com/user-attachments/assets/fc3154ad-622f-4e2b-96e6-d0873171d316" />

tar -xvf backup.tar
## OUTPUT

<img width="1444" height="768" alt="image" src="https://github.com/user-attachments/assets/3d988270-2aa5-414a-aa69-4aeacddb513f" />

# RESULT:
The Commands are executed successfully.
