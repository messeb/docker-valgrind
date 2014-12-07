Valgrind Docker environment
===========================

Docker environment with gcc and valgrind


### build the docker image
	
	$ sudo docker build --rm --tag valgrind .
	
	
### run the docker container

	$ sudo docker run --hostname valgrind --name valgrind -v [local/sourcecode/path]:/root/build -d -p 22021:22 valgrind
	
Replace [local/sourcecode/path] with the path to your source code on your host
	
### enter the container

	$ ssh -p 22021 root@localhost  # password = root
	$ cd ~/build
	
Now, you have your source code from your host mounted in the container (~/build) and you can compile and test it.