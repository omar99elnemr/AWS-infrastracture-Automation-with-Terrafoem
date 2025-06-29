# Terraform AWS Web Server Infrastructure

A simple project where I learned to deploy web servers on AWS using Terraform.
![image](https://github.com/user-attachments/assets/d6fd79bd-0311-4a6c-ad7b-1eb4ba0868ef)


## What This Project Does

This creates a basic web server on AWS that shows a colorful "My Portfolio" page with the server's ID.

## What I Built

- A web server running on AWS EC2
- A simple HTML page with color-changing text
- Everything deployed using Terraform code

## Files in This Project

- `provider.tf` - Tells Terraform to use AWS
- `variables.tf` - Sets the network settings
- `userdata.sh` - Script that installs Apache web server
- `userdata1.sh` - Another version of the setup script

## Before You Start

You need:
- Terraform installed on your computer
- An AWS account
- AWS CLI set up with your credentials

## How to Run This

1. **Download this project**
   ```bash
   git clone <your-repo-url>
   cd <project-folder>
   ```

2. **Set up AWS**
   ```bash
   aws configure
   # Enter your AWS Access Key, Secret Key, and region
   ```

3. **Run Terraform commands**
   ```bash
   terraform init    # Downloads what Terraform needs
   terraform plan    # Shows what will be created
   terraform apply   # Actually creates everything
   ```

4. **Find your website**
   After it finishes, Terraform will show you the web address where you can see your page.

## What the Website Shows

- A title that changes colors (red → green → blue)
- The server's unique ID number
- A welcome message

## To Clean Up

When you're done testing:
```bash
terraform destroy
```
This deletes everything so you don't get charged.

## What I Learned

- How to write basic Terraform code
- How to launch servers on AWS
- How to automatically install software on new servers
- How infrastructure as code works

## Notes

- The server runs in the us-east-1 region
- It uses a 10.0.0.0/16 network (you can change this in variables.tf)
- The web server starts automatically when the instance boots up

## Issues I Faced

- Had to make sure AWS credentials were set up correctly
- Learned that destroying resources is important to avoid charges
- Found out that security groups need to allow web traffic

---

This is my learning project for understanding AWS and Terraform basics!
