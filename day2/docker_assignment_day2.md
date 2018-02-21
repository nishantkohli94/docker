Assignment 1:

1. Create/Run a container from "ubuntu" image and take interactive shell inside it.
2. Once you would be inside container, run below commands.
	apt-get update
	apt-get install -y figlet
	figlet "hello docker"
    exit
3. Inspect all the changes that you have done inside container using container ID.
4. Commit your container for the changes that you have made.
5. List docker images to check the image that got created after commit.
6. Tag newly created image using image id and tag name should be "ourfiglet".
7. Run a new container using newly created image "ourfiglet".
8. Take bash shell on the running container and run below command. Command should output "hello" in ascii form.
	figlet "hello"


Assignment 2:

1. Create a file named index.js with below content.

index.js
----------------
var os = require("os");
var hostname = os.hostname();
console.log("hello from " + hostname);

2. Create a file named Dockerfile and write code as per the steps mentioned.

a. Use alpine image.
b. run commands -> apk update & apk add nodejs
c. copy current directory to /app
d. change your working directory to /app
e. specify the default command to be run upon container creation as mentioned below.
	node index.js
	
3. Build image from Dockerfile and tag it with name "hello:v0.1"
4. Append below line in index.js
	echo "console.log(\"this is v0.2\");" >> index.js
5. Now build an image from Dockerfile and tag it with name "hello:v0.2"