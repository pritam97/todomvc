1. Login to VM Via 
ssh 139.59.89.2 -p 6621 
output:
login as: joe
joe@139.59.89.2's password:
[joe@centos-74 ~]$
------------------------
2. checking oS version using below command & available files in home directory. 
[joe@centos-74 bin]$ cat /etc/redhat-release
CentOS Linux release 7.4.1708 (Core)
[joe@centos-74 ~]$ ls
node-v8.9.4-linux-x64  todomvc
 
Node software & todomvc application is ready. 
----------------------------------------------------------
3.  for running node & npm command we need to set node environment. then npm command will work. 

This command will set the node environment. 
export PATH=$PATH:/home/joe/node-v8.9.4-linux-x64/bin
[joe@centos-74 todomvc]$ node -v
v8.9.4
[joe@centos-74 todomvc]$ npm -v
5.6.0


   ╭─────────────────────────────────────╮
   │                                     │
   │   Update available 5.6.0 → 5.7.1    │
   │     Run npm i -g npm to update      │
   │                                     │
   ╰─────────────────────────────────────╯

------------------------------------------------------
4.Adding todomvc Application into GIT 

git config --global user.name "pritam97"
git config --global user.email "pritamkosalage97@gmail.com"
cd /home/joe/todomvc/
git add . # this will add your files available in local to git repository.
git commit -m "uploading todomvc application"
git remote add origin https://github.com/pritam97/todomvc.git
git push -u origin master
-----------------------------------------------


5.npm install 
[joe@centos-74 todomvc]$ npm install
npm WARN todomvc@0.1.1 No repository field.
npm WARN todomvc@0.1.1 No license field.

updated 1 package in 12.644s

-------------------------------------------------------
6. to start application 

[joe@centos-74 todomvc]$ npm run test-server

> todomvc@0.1.1 test-server /home/joe/todomvc
> gulp test-server &

[joe@centos-74 todomvc]$ [13:24:32] Using gulpfile ~/todomvc/gulpfile.js
[13:24:32] Starting 'test-server'...
[13:24:32] Finished 'test-server' after 4.55 ms
----------------------------------------------------------------
7.simple script to get HTTP code. 
[joe@centos-74 todomvc]$ curl -o /dev/null --silent --head --write-out '%{http_code}\n' http://139.59.89.2:3000
200
---------------------------------------------------------------

8. attached browser Image in GIT repository.
-----------------------------------------------------------
9 & 10 is tough for me to do. 
-----------------------------------------------
 created file using below command 
vim TASKS.md. 
git add TASKS.md  # this will add your TASKS.md file available in local to git repository.
git commit -m "uploadiing TASKS.md file"
git remote add origin https://github.com/pritam97/todomvc.git
git push -u origin master
-------------------------------------------------------
11.
Technology Used: 
1. Linux OS 
2. node 
3. npm 
4. angular 2 
5. bash script 
6. phatomjs 
7. Java Script. 
8. git  SCM tool. 
resources.:
Node Site: - https://nodejs.org/en/
Git Site - https://git-scm.com/
 
---------------------------------------------------------
12. Added TASK.md file into repository. 
---------------------------------------------------------

-------End-------------------------
