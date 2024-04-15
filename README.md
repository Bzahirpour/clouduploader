# Bash-based CLI toold that allows users to quickly upload files to s3
I wrote this tool as part of my studies for cloud engineering. The project came from the website [Learntocloud](https://learntocloud.guide/phase1/) section 1 which covers Linux and networking. The website outlines a study path broken into sections, and at the end of each section a project is givin to put into practice the topcis learned in the section. The objective is outlined on the website, but there is no guide so you're left on your own to figure out how to complete the project. The project encompasses knowledge of BASH, Linux, and AWS.

## Prerequisites

- [An AWS subscription. Create one for free.](https://aws.amazon.com/resources/create-account/)
- [Install WSL if you are on Windows. Skip if you are on Linux.](https://learn.microsoft.com/en-us/windows/wsl/install)
- [Create access keys inside of IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)
- Configure aws - open wsl and run "aws configure", then copy / paste the access key into the CLI, and copy paste the secret key into the CLI. For the default region select a region close to you for me its us-east-1, default output format just press enter.

## How to setup

1. Create a bucket in aws through the CLI: "aws s3 mb s3://clouduploader-yourbucketname"
2. Take the bucket name and replace the name of the bucket inside of the script (mine is called clouduploader-bnz)
3. Change the permissions on the script "chmod 744 clouduploader" (Makes the file executable)
4. Place this script in ~/bin directory, where personal executable files such as scripts are intended to be stored.

## How to use

1. Type clouduploader in the shell. The first arguement is name of the file you wish to upload.
2. Example: "clouduploader myfile.txt"

## How it works

The file name you enter will get copied to the s3 bucket named "clouduploader". Before the file is uploaded the script will check to make sure the file exists. There will be a progress bar to indicate the status of the upload, and the script will let you know if the file has been successfull uploaded or not.


## Contributing

Feel free to open up an issue or reach out to me.

 **Benjamin Zahirpour**
