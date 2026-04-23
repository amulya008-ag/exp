# exp

Exp 11

Open Eclipse → New Java project →name it as Addition → save it.
Go to src → right click → New → java class →
Package- addition example
name class as Addition. 
source folder-addition/src
Finish

Put a code

Go to Addition → right click → Build path →
Add lib → JUnit → Finish for JUnit5

It will look like:
Addition
 JRE System lib
 JUnit5
 src
  addition example
  module-info

Go to src → right click → New → JUnit test case.
Name - AdditionExampleTest → Finish
paste test code → save
Right click on code part in test file
run as → JUnit test case → Green

⸻

Exp 12

cmd

1. mvn –version
2. mvn archetype:generate
3. choose a num - 9
4. gId: com.bnm.it
5. AId: sample
6. yes
7. after cheecking if all the files are there come back to cmd and run cd sample
8. mvn package
9. go to app.java in the files, src-main-calci and paste code
10. src-test-aootest.java paste testing code and save
goto cmd
11. mvn clean test
    after every change in the code run
    mvn clean test command in cmd

⸻

Exp 13

Open jenkins, github
Create a repository
Add files pom, src those 3 files except mvn one(select and add)

Jenkins → New item → Maven project →
Discard old builds → 5 5 → source code manage
→ Git → Branch specifier (main) → poll SCM →
Schedule * * * * * → run only if build success

Build →Root → pom.xml
Goals & options → package → save

Add (scribbled)

Build now

Configure now → Archive the artifacts in
post build steps → click on ? mark copy paste

⸻

Exp 14

mvn archetype:generate

src → main → java → com → App
src → test → App test

cd sample
mvn package
(target file will be created) → check

go to pom open it with VS Code
<build>  
  → Add code before  
<plugin management>  

save

mvn clean test

goto → target → site → jacoco → open index.html
→ show the report like

If 100% is shown to ask
72% is covered 50% is left out

Increase it to 100%

Open src test folder add extra part to the code

mvn clean test

⸻

Exp 15
put docker commands
Ξ → Traffic/port → open new tab → click on
your port 8080 → welcome to nginx

commands
docker version containers prune to delete
everything

⸻

Exp 16

mkdir dockerapp
cd dockerapp

nano app.py
Paste code

nano Dockerfile
paste code

docker build -t mypythonapp . 

docker run -d -p 5020:5020 nginx

Ξ → Ports → 5020 port → output

docker ps

⸻

Exp 17

docker run -d nginx
docker run -d -p 8082:80 nginx    (both only for port mapping)

1. docker volume create myvolume
2. docker volume ls
3. docker run -it -v myvolume:/data ubuntu bash
4. cd /data
5. echo “Docker volume test” > test.txt
6. exit
7. docker run -it -v myvolume:/data ubuntu bash
8. cat /data/test.txt
10. exit
11. docker run -d -p 8083:80 -v myvolume:/usr/share/nginx/html nginx
12. docker run -it -v myvolume:/data ubuntu bash
13. echo “<h1>Persistent web</h1>”/data/index.html
14. Go to ports and access

⸻

Exp 18

mkdir dockerjava
cd dockerjava
nano Main.java
nano Dokerfile

docker build -t javaapp .<space> 

docker run -d javaapp

docker login

docker tag javaapp <username>/java-app:v1

docker push <username>/java-app:v1

docker pull <username>/javaapp:v1

docker run -it <username>/javaapp:v1

Docker images

⸻

Exp 19

Add jenkinsfile & push the main, docker, jenkins to git
Add code

Go to Jenkins → pipeline → select pipeline

enter github url
build now

EXP 20
Create a folder exp20 in file exp
Open gitbash

cd Desktop
cd exp 20

git clone 
delete .git file in files

⸻

git init

git config –global user.name
email

git add .

git commit -m “Initial commit”

git remote add origin 

git remote remove origin → if origin exists shows.

git push -u origin main

⸻
