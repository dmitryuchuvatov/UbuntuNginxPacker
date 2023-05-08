# Create an AMI using Packer (Ubuntu with Nginx)

# Prerequisites
Install and configure Packer as per [official documentation](https://developer.hashicorp.com/packer/tutorials/docker-get-started/get-started-install-cli)

Configure [AWS credentials](https://developer.hashicorp.com/packer/plugins/builders/amazon)

# How To

## Clone the repository

```
git clone https://github.com/dmitryuchuvatov/ubuntunginxpacker.git
```

## Go into the directory

```
cd ubuntunginxpacker
```

## Initialize Packer

```
packer init .
```

You should see the similar output:

```
Installed plugin github.com/hashicorp/amazon v1.2.5 in "/Users/dmitryuchuvatov/.config/packer/plugins/github.com/hashicorp/amazon/packer-plugin-amazon_v1.2.5_x5.0_darwin_arm64"
```

## Build AMI

```
packer build .
```
When prompted, enter the desired region and hit **Enter** to confirm:

```
==> ubuntu-nginx.amazon-ebs.ubuntu-nginx: Prevalidating any provided VPC information
==> ubuntu-nginx.amazon-ebs.ubuntu-nginx: Prevalidating AMI Name: ubuntu-nginx
    ubuntu-nginx.amazon-ebs.ubuntu-nginx: Found Image ID: ami-0a0a0efaa60d3479f

...

Build 'ubuntu-nginx.amazon-ebs.ubuntu-nginx' finished after 3 minutes 26 seconds.
```

## Navigate to Amazon Machine Images (AMIs) page on AWS and check the results:

![Screenshot 2023-05-08 at 10 30 51](https://user-images.githubusercontent.com/119931089/236776103-35aebc3e-673e-4856-a147-68d2bd74c83c.png)
