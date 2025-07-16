# Docker_Documentation

##  Docker Commands

### Pull Image
`` docker image pull <image_name>``
### List docker images 
``` dokcer images ```
### Remove / delete image
Just delete an image. This does not work if a container is already created with that image, even if it has stopped.
  
``` docker image rm <image_name> ```

To force remove the image.

``` dokcer image rm -f <image_name> ```

### To run image as a container
this comands just runs and exits.

~~~
docker container run <image_name>
~~~

For interation and terminal, run the below.
~~~
docker run -it <image_name> 
~~~
- _-i - for interactive_
- _-t - for terminal_

To run an image as a container with custom name

``` docker run --name <your_container_name> <image_name> ```

### List docker containers

The command only list the running containers
~~~
docker container ls
# or
docker ps
~~~

To list all the containers 

``` docker ps -a ```

### To start/ stop a container

- start a container
~~~
docker container start -i <container_name>
~~~
- stop a container
~~~
docker container stop <container_name>
~~~

### Remove container container
- to remove a container

``` docker container rm <container_name> ```

### Open new terminal for existing container

``` docker exec -it <container_name> ```

- to remove all the containers

``` docker container prune ```

### To build an image
to build an image for with custom name

``` docker image build -t <my_image_name> <path_to_dockerfile> ```
