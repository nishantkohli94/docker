Run a docker container from "hello-world" image.


docker run hello-world

Pull "alpine" image from docker registry and see if image is available in your local image list.


Using default tag: latest
latest: Pulling from library/alpine
8e3ba11ec2a2: Pull complete
Digest: sha256:7043076348bf5040220df6ad703798fd8593a0918d06d3ce30c6c93be117e430
Status: Downloaded newer image for alpine:latest

Pull some specific version of docker "alpine" image from docker registry.


docker pull alpine:3.3

Run a docker container from local image "alpine" and run an inline command "ls -l" while running container.

docker run -it alpine ls -l


Try to take login to container created using "alpine" image.

docker run -it alpine /bin/ash

ctrl + p +q


Check running containers and see if you can find out the stopped containers.

docker ps -a
CONTAINER ID        IMAGE               COMMAND              CREATED             STATUS                      PORTS               NAMES
fe2e96dc5c45        alpine              "/bin/ash"           56 seconds ago      Up 56 seconds                                   dreamy_meitner

Stop running container.
docker stop fe2e96dc5c45


Start container that was stopped earlier.

docker stop fe2e96dc5c45


Try to remove "alpine" image from your local system.

docker rmi alpine
Error response from daemon: conflict: unable to remove repository reference "alpine" (must force) - container 2ecee6e1d6dc is using its referenced image 11cd0b38bc3c


