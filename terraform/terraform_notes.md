# Terraform Notes <!-- omit from toc -->

# :link: Table of Contents <!-- omit from toc -->
+ [Module 3](#%6D%6F%64%75%6C%65%2D%33)
  + [Overview](#%6F%76%65%72%76%69%65%77)
  + [Installation](#%69%6E%73%74%61%6C%6C%61%74%69%6F%6E)
  + [Terraform Object Types](#%74%65%72%72%61%66%6F%72%6D%2D%6F%62%6A%65%63%74%2D%74%79%70%65%73)
  + [Block Syntax](#%62%6C%6F%63%6B%2D%73%79%6E%74%61%78)


## Module 3
### Overview
- What is Terraform?
  - Core Components 
  - Workflow
  - Installation

### Installation 
- Download the executable for your platform
  - Add to your PATH environment variable.
  - Share and enjoy!

Below are steps on how to install on 3 platforms, **macOS**,**Windows** and **Linux**. 

<details>
  <summary>Click Here</summary>

- **macOS**
```zsh
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

- **Windows**
```pwsh
winget install Hashicorp.Terraform
```
You can also download the zip file located [here](https://releases.hashicorp.com/terraform/1.9.2/terraform_1.9.2_windows_amd64.zip) and do the needful.

- **Linux**
<details>
  <summary>Click Here</summary>

- **Ubuntu/Debian**
```bash
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
```
- **CentOS/RHEL/Fedora/Amazon Linux**
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
sudo yum -y install terraform
```
</details>
</details>

After installing Terraform it is a good idea to check the version. this can be done with a simple
```
$ tf version
Terraform v1.9.2
on linux_amd64
```
The output should look something like this. 

### Terraform Object Types
- Providers
- Resources
- Data sources
  
### Block Syntax
> [!NOTE]
> Terraform uses block type syntax below is an example

-  **main.tf**
```tf
 resource "aws_instance" "web_server" {
    name = "web-server"
    ebs_volume {
        size = 40
    }
 }
 ```

- Terraform Object Refrence
```tf
aws_instance.web_server.name
```









