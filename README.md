Task 1 : EC2 Ubuntu Instance

Step 1: Launch or Use an Existing EC2 Instance

Log in to the AWS Management Console
Navigate to EC2 > Instances
Launch a new Ubuntu instance or use an existing one
Choose Ubuntu Server (e.g., Ubuntu 20.04 LTS)
Select instance type (e.g., t2.micro)
Select or create a Key Pair (download the .pem file)
Ensure the Security Group allows SSH (port 22)

Step 2: Connecting VSCode to your EC2 Instance

Install remote ssh
Select the option ‘Connect to Host’
Then, select the configuration file that starts with ‘/Users/..’
Then, you’re brought to a config.ssh file that allows you to edit information on it

Host 44.201.230.32
    HostName 44.201.230.32
    User ubuntu
    IdentityFile ./key/practice-instance-1.pem

Save the changes and click on connect

Step 3: Create a New User on the EC2 Ubuntu Instance

Run the following: sudo adduser yourname 
Grant the new user sudo privileges:
sudo usermod -aG sudo yourname
Switch to the new user:
sudo su - yourname

--------------------------------------------------------------------------------

Step 1 :Start your existing instance
        SSH into the instance:


Step 2 :Clone the Repository
        git clone https://gitlab.com/sty_projects/devops_interns/interns_devops.git
	cd interns_devops

Step 3 :Checkout the feature Branch
	git checkout feature

Step 4 :Create a New Branch From feature
	Replace yourname with your actual name or identifier:
	git checkout -b yourname-feature

Step 5:Deploy Using Docker and Docker Compose on Port 3009

Step 6:Push Code to GitLab
	git add .
	git commit -m "Deployed branch on port 3009 and updated docker-compose"

	Push your branch:
	git push origin yourname-feature

git checkout feature , git checkout -b name feature 
git add . 
git commit -m "changes have been made"

git push origin yourname feature 
git checkout feature 
git checkout -b yourname feature
git add .
git commit -m "deployed branch"

git branch 
git checkout feature 
git checkout -b yourname feature
git add .
git commit -m "Final change"

git clone 
git checkout feature
git checkout -b 

---------------------------------------------------------------------------------
EBS volume

Step 1: Launch the EC2 Instance
Login to AWS Management Console.
Navigate to EC2 Dashboard > Click Launch Instance.
Configure the instance:
Name: EBS_eg
Instance Type: t2.micro (or as required)

Network Settings > Create or choose an existing Security Group:
Add Inbound Rules:
Type: Custom TCP | Port: 3009 | Source: 0.0.0.0/0
Type: Custom TCP | Port: 3000 | Source: 0.0.0.0/0
Type: HTTP | Port: 80 | Source: 0.0.0.0/0
Click Launch Instance.

Step 2: Add and Attach a 10 GB EBS Volume
Go to Elastic Block Store > Volumes > Click Create Volume:
Size: 10 GiB
Type: General Purpose (gp3)
Availability Zone: Same as EC2 instance
After creation, select the volume > Actions > Attach Volume:
Select the EC2 instance

------------------------------------------------------------------------------------


