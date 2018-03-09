# Description

This docker container contains an Ubuntu 14.04 sshd server. The name of the project is test_ssh_server.

This small project is under development.

# Use

Build the docker image with the command:

`docker build -t test_sshd .`

Once the inage is created, run the image with the command:

`docker run -d -P --name eg_sshd test_sshd`

Check that the 22 port is present whith the command:

`docker port test_sshd 22`

You can inspect the docker machine to find the IP address of your sshd server:

`docker inspect eg_sshd | grep IPAddress`

Now you can connect via ssh:

`ssh sshtest@IPAddress`

Use `testpswd` as password

