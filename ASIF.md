# Git & GitHub Task 20231021


## Tasks List

**Please click on any Task to directly go to the list of activities.**



## Prerequisite
- [Create a GitHub account](https://github.com/rise2innovate). (Skip, If you have done already) <br>
- Add both of the following ways to authenticate to push to your repositories: <br>
-- [**SSH**](#SSH): generate and add a public/private SSH key pair to GitHub. [GitHub tutorial](https://drive.google.com/file/d/1tL4FvtwaVLio9h1qyQT18EhGyeQ7DNxf/view?usp=share_link) <br>
-- [**HTTPS**](#HTTPS): generate and save a GitHub token to connect with HTTPS: (We have already learnt and implemented)

### Tasks

1. [Install Git or Github Desktop on your PC](#Task1)
2. [Download the website from following url in a directory https://www.free-css.com/free-css-templates/page296/carvilla using linux command.](#Task2)
3. [Make commit of whole data with name "initial commit"](#Task3)
4. [Make remote access of github repository.](#Task4) 
5. [Now commit this code to github in a reposity in main branch.](#Task5)
6. [Add some changes in your websites (stored in your PC , that was downnladed from https://www.free-css.com/free-css-templates/page296/carvilla)](#Task6)
7. [Now again repeat procedure of push to Github so changes can be visible on your repo](#Task7)
8. [Clone repo https://github.com/engineerbaz/docker-file.git in /temp/testRepo](#Task8)
9. [Make a repo of your own name and make two branches in it as `prod` and `dev`](#Task9)
10. [Fork the repository (https://github.com/engineerbaz/DevOps-09-Training/) by clicking on the Fork button on the upper right corner](#Task10)
11. [Clone the repository of your fork with: git clone https://github.com/YOURLOGIN/DevOps-09-Training (replace YOURLOGIN with your GitHub login)](#Task11)
12. [Create a file of your Task in Markdown language and upload.](#Task12)     
  

---
&nbsp;
&nbsp;
---
&nbsp;
&nbsp;


# Tasks activities and submission

### Prerequisites

1. [GitHub account created](https://github.com/rise2innovate) 
2. Authentication added   
#### SSH
    
Generating SSH Key:

```bash
ssh-keygen -t ed25519 - C "rise2innovate@gmail.com"
```
**Output:**

![SSH Key Generation Locally](./PR1.png)

Starting SSH Service manually:

```bash
Get-Service ssh-agent
```

**Output:**

![Starting SSH service Manually](./PR2.png)



Adding new public key to GitHUB:

**Output:**

![Adding SSH Key in Github](./PR3.png)



Verification on Github:

**Output:**

![Verifying SSH Key in Github](./PR4.png)


#### HTTPS

Generating HTTPS Personal Token:

**Output:**

![Personal Access token](./PR5.png)  

&nbsp;
---
&nbsp;
&nbsp;
---
&nbsp;
&nbsp;  


___
### Task1
*Install Git or Github desktop on your PC.*


Git bash is already installed on PC.

---
&nbsp;

### Task2: 
*Download the website from following url in a directory https://www.free-css.com/free-css-templates/page296/carvilla using linux command*

Linux command to download a webpage:

```bash
curl -O https://www.free-css.com/free-css-templates/page296/carvilla
```

**Output:**


![Download website using Linux command](./task2.png)


---
&nbsp;

### Task3
*Make commit of whole data with name "initial commit"*

```bash
git add .
git status
git commit -m "initial commit"
```

**Output:**

![initial commit on local Git](./Task3.png)


---
&nbsp;

### Task4
*Make remote access of github repository.*

Create a repo on Github:

**Output:**

![Download website using Linux command](./Task4a.png)


Check if any other remote repo is connected:

```bash
git remote -v
```

Access you remote repo to local Git:

```bash
git remote add origin https://github.com/rise2innovate/gitassignment.git
```

Validate if the remote repo is now visible:

```bash
git remote -v
```
**Output:**

![Connecting to remote repo](./Task4b.png)


---
&nbsp;

### Task5
*Now commit this code to github in a reposity in main branch.*

Setting up the origin upstream (using -u switch):

```bash
git remote -u origin main
```

Pushing the code to Github in the remote repository in main branch:

```bash
git push -u origin main
```

**Output:**


![Pushing code to Github](./Task5a.png)


Verifiying the push at Github repo:

![Verification on Github](./Task5b.png)


---
&nbsp;

### Task6
*Add some changes in your websites (stored in your PC , that was downnladed from https://www.free-css.com/free-css-templates/page296/carvilla)*  



Modified the file using VS code:
**Output:**

![Perform modification on file](./Task6a.png)

Commit the file changes locally:

```bash
git add .
git commit -m "carvilla file changed"
```

**Output:**

![Commit changes locally](./Task6b.png)


---
&nbsp;

### Task7
*Now again repeat procedure of push to Github so changes can be visible on your repo*

Pushing the local commits to Github:

```bash
git remote -v
git push origin main
```

**Output:**

![Pushing commit to Github](./Task7a.png)


Verifying the changes on Github:

![Changes verification on Github](./Task7b.png)


---
&nbsp;

### Task8
*Clone repo https://github.com/engineerbaz/docker-file.git in /temp/testRepo*

```bash
pwd
mkdir /e/git/temp
git clone https://github.com/eigineerbaz/docker-file.git /e/git/temp/testRepo
```

**Output:**

![Cloning remote repo to local directory](./Task8a.png)


![Verifying the clone repo in local directory](./Task8b.png)



---
&nbsp;

### Task9
*Make a repo of your own name and make two branches in it as `prod` and `dev`*

Initiating a new local repo named "Asif":

```bash
git init
git add .
git commit -m "first commit"
git status
```

**Output:**

![Initiating new local repo with first commit](./Task9a.png)

 Creating branches, verifying and switches between them:


```bash
git branch
git branch prod
git branch dev
git branch
git checkout prod
git brnach
```

**Output:**

![New branching](./Task9b.png)


---
&nbsp;

### Task10
*Fork the repository (https://github.com/engineerbaz/DevOps-09-Training/) by clicking on the Fork button on the upper right corner*


**Output:**

![Forking the public repo](./Task10.png)


---
&nbsp;

### Task11
*Clone the repository of your fork with: git clone https://github.com/YOURLOGIN/DevOps-09-Training (replace YOURLOGIN with your GitHub login)*

Initiating a new Repo locally:

```bash
git init
git status
git add .
```

**Output:**

![Initiating a new Repo locally](./Task11a.png)

Connecting remote repo that was forked from other user:

```bash
git remote add https://github.com/rise2innovate/DevOps9thBatch.git
git remote -v 
```

**Output:**

![Connecting remote repo](./Task11b.png)


Cloning the remote repo:

```bash
git clone https://github.com/rise2innovate/DevOps9thBatch.git
ls -al
```

**Output:**

![Cloning the remote repo](./Task11c.png)


Pushing changes to Github:

```bash
git add .
git commit -m "changes to asif.md file"
git status
git push -u origin main

```

**Output:**

![Push to Github](./Task11d.png)


Verifying changes on Github:

**Output:**

![Github status check](./Task11e.png)


Creating a Pull Request to the owner of repo:


**Output:**


![Creating a Pull Request](./Task11f.png)

PR raised:

**Output:**

![Pull Request raised](./Task11g.png)


---
&nbsp;

### Task12
*Create a file of your Task in Markdown language and upload.*

[ASIF.md](https://github.com/rise2innovate/Asif/blob/main/ASIF.md) file created and uploaded to Google classroom assignment.
