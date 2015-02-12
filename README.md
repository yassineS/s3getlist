s3getlist
=========

[![Join the chat at https://gitter.im/yassineS/s3getlist](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/yassineS/s3getlist?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A simple script that allows the user to download a list of files from an AWS S3 bucket.

s3getlist takes as input a text file containing a list of files on S3 (full path) and download it to a given directory.

***Warnings:***
Make sure that you have access to the specified S3 buckets.
Make sure that the download directory exists.

**INSTALLATION**
To install s3getlist you need to download the repository on your machine and run the INSTALL script with admin access:

    git clone git@github.com:yassineS/s3getlist
    cd s3getlist
    sudo ./INSTALL
    
During the installation process you will need to configure the *s3cmd*:

You will be asked for the two keys - copy and paste them from your confirmation email or from your Amazon account page. Be careful when copying them! They are case sensitive and must be entered accurately or you'll keep getting errors about invalid signatures or similar.

You can optionally enter a GPG encryption key that will be used for encrypting your files before sending them to Amazon. Using GPG encryption will protect your data against reading by Amazon staff or anyone who may get access to your them while they're stored at Amazon S3.

Another option to decide about is whether to use HTTPS or HTTP transport for communication with Amazon. HTTPS is an encrypted version of HTTP, protecting your data against eavesdroppers while they're in transit to and from Amazon S3.

Please note: - both the above mentioned forms of encryption are independent on each other and serve a different purpose. While GPG encryption is protects your data against reading while they are stored in Amazon S3, HTTPS protects them only while they're being uploaded to Amazon S3 (or downloaded from). There are pros and cons for each and you are free to select either, or, both or none. Refer to s3cmd encryption HowTo for more details.

Source: http://s3tools.org/s3cmd
    
**Usage**
s3getlist is very simple to use and consists of a single command. The syntax is the following:

    s3getlist /path/to/the/file/list /path/of/destination
