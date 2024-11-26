# Capstone Project-Introduction to Cloud Computing
## Capstone Project: E-Commerce Platform Deployment with Git, Linux, and AWS.

### Introduction:

Developing an e-commerce website for a new online marketplace named **MarketPeak**. This platform will feature product listings, a shopping cart, and user authentication.

### Project Implementation:

I will use Git for version control and the  development space will be in a Linux environment, and deploy it on an AWS EC2 instance and a templete for website has been provided so i dont need to create from scratch.

### Task

**1: Implement Version Control with Git**

Initialize a Git Repository: Creating the project directory and name it "*MarketPeak_Ecommerce*", Then cd into the new project directory and initialize s a git repository. 

See image below:

`mkdir MarketPeak_Ecommerce`
`cd MarketPeak_Ecommerce`
`git init`

![alt text](images/Mkdir-CD-gitadd-init-Directory.png)

**1.i. Get Source code from template.com:**
1.ii. Obtain and Prepare the E-Commerce Website Template: As a devops engineer i don't need to write website codes, This is the work of a software developer and all i have to do is to dowload the existing E-commerce website template.

**1.iii. Downloading a Website Template:** Visit [Tooplate](https://www.tooplate.com) to download any suitable E-Commerce website template, you can also use other sites to do so.

The below images shows how it was downloaded to my local system.

![alt text](<images/Template site.png>)
![alt text](<images/Download Template.png>)

The Zipped file was downloaded on my Local PC and i was able to unzip it on my Mac GUI (Graphical user interface), I then copy the extracted folder to the Directory (MarketPeak_Ecommerce) created on my version contron terminal.

**2: Stage and Commit the Template to Git:** This is the process of making git aware of the new items added and futher to commiting any changes been made and a description will be added to it anytime the commit is been performed.

See below image:

`git add .`
`git commit -m "Code files for Marketpeak"`

![alt text](images/Git-Commit.png)

**3: Pushing the code to Github repository**

So far, I’ve been able to allow Git to track and monitor all the project work done locally on my system but that's is not enough, I need to create a github repository online naming it *MarketPeak_Ecommerce* and push from my local remote to the GitHub remote created online should incase my system brakes down or crashed, I can always go to the online repository created to recover my projects.

**3.i: Creating a Remote Repository on GitHub:**

The below images shows how i created my git repository named *MarketPeak_Ecommerce*

![alt text](images/Creating-newrepo-on-github-MarketPeak_Ecommerce.png)

**3.ii. Linking my Local Repository to GitHub:** Navigated to the project directory (MarketPeak_Ecommerce)in my VS terminal and added the remote repository URL to my local repository configuration.
`git remote add origin https://github.com/bolajidevops/MarketPeak_Ecommerce.git`

![alt text](images/Link-local-github&pushing-all-files.png)

**3.iii. Pushing my code to GitHub repository:** The command below is used to carry out this task.
`git push -u origin main`

![alt text](images/Link-local-github&pushing-all-files.png)

See image above for better understanding of git cloning and pushing to github repository.


## Step 2: AWS Deployment

**Task 1: Setup an AWS EC2 instance for deployment**

- I Logged in to my AWS Management Console.
- I Launched an EC2 instance using an Amazon Linux AMI.
- Connecting to the instance using SSH.

![alt text](images/Launching-EC2-AWS.Linux.png)

![alt text](images/Connecting-Instance:SSH.png)

**Task 2: Cloning the repository on the AWS Linux Server**

I need to clone the GitHub repository to my AWS EC2 instance Before deploying my e-commerce platform. This has to do with authenticating with GitHub and there are two ways to do that which are SSH Cloning and HTTPS cloning For the sake of this project i will be using the SSH method.

**2.i Authenticating with GitHub using SSH:** On my Linux EC2 instance, i generated SSH keypair using ssh-keygen as shown below:

![alt text](images/Generating-Keygen.png)

**2.ii Cat and copy the public key**

`cat /home/ec2-user/.ssh/id_rsa.pub`

**2.iii. Adding SSH Public key to GitHub repository:**

Navigate to my image icon On my github account, Clicked on sttings, then click on SSH and GPGKeys.

![alt text](images/Adding-Keygen-Github.png)

**Note:** This is a AWS Linux server by default git is not installed, so i have to run the command below to install git

`sudo yum install git -y`

`git clone git@github.com:bolajidevops/MarketPeak_Ecommerce.git`

![alt text](images/Cloning-git-EC2Linux-terminal.png)














