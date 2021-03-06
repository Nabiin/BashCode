# Basic Command


---
---



# Node js
To debug node application  we should to
1. Add <mark> debugger </mark> keyword anywhere in code
1. Then in terminal fired following command
 ```bash
 $ node --inspect-brk filename.js
  or
 $ node --inspect filename.js
 ```

---
---


# Heroku
>Download and install heroku setup from the link below

https://devcenter.heroku.com/articles/heroku-cli#download-and-install

After installing :-

---

To see the version installed
```bash
$ heroku -v   
```
To login
```bash
$ heroku login
```
>> Please Scroll down to  SSH topic and create your ssh command to your machine and continue this step

To use ssh public key to heroku 
```bash
$ heroku keys:add
$ y
```
## Create Heroku Application
To create heroku app your project must be uploaded to Github first , if so then Go the root of the Project and fire following
command :-
```bash
$ git remote
// Origin
//heroku  this remote must be shown after git remote command
```

```bash
$ heroku create <filename>
$ heroku create nabin-weather-app 
```
The file name should be unique and identifying so that all the heroku application should be known
> $ heroku create nabin-weather-app 


## .env setup
The regular way to set up environment variables is
```bash
$ heroku config:set key=value
```
To see the configuration
```bash
$ heroku config
//this will show all the config of .env
```
To remove the configuration
```bash
$ heroku config:unset key
```
For complete Example:-
```bash
//To add 
$ heroku config:set jwt=demoStringsExmple

//To view
$ heroku config

//To remove or unset
$ heroku config:unset jwt
```
And push to heroku as same as pushing to Github
```bash
$ git push heroku master
```
---
---
# MongoSetup
## Whitelist a connection IP address
>add a different ip address

0.0.0.0/0

>>save db id and password
---
---
 # SSH
> This is only for Windows machine
## To search SSH folder
```bash
$ ls -a -l ~/.ssh
```
1. <mark>ls </mark> list out all of the files in the directory
1. <mark>-a</mark> is used to show all the files including hidden file and folder
1. <mark> -l </mark> list everything top to button (format easire us to list )

## To generate SSH key pair
```bash
$ ssh-keygen -t rsa -b 4096 -C "your email address"
```
1. <mark>ssh-keygen</mark> This allows us to generate the pair of ssh key
1. <mark>-t</mark>  this stand for type , to use protocal
1. <mark>rsa</mark> rsa is a protocal ,
1. <mark>-b </mark> for bits , we have provide 4096 bits for this demo
1. <mark>-C</mark> this C is a capital C , which is used as a comment 

## To check the Program is running
```bash
$ eval $(ssh-agent -s)
```
This wil give the agent pid id

## Register the file securely
```bash
$ ssh-add ~/.ssh/id_rsa
```

---
---


# How to connect ssh key to Github
1. In Github Go to Setting > Personal Setting > SSH and GpG key then
1. Give ssh key Title (any) and then go to bash terminal and hit
```bash
$ cat ~/.ssh/id_rsa.pub
```
3. Then copy all the (long) key  from the terminal  and paste them  key section 

 *****   And you done   **********
## To see ssh connection to the git  hub server
```bash
$ ssh -T git@github.com
```



---
---


# How to connect ssh key to heroku
## Setup SSH public key file to the heroku
To use ssh public key to heroku 
```bash
$ heroku keys:add
$ y
```
