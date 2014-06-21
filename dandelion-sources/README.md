dandelion-docker
================

Dockerfile of [Dandelion-Core](https://github.com/dandelion/dandelion), used to set up a build environment.

The environment is based on CentOS 6.4 and contains:

 * OpenJDK 6
 * Maven 3.2.1 
 * PhantomJS 1.9.7 

## Usage

Pull the image

````
docker pull tduchateau/dandelion-sources:0.10.0
````

Run a new container from this image:

````
docker run -p 4022:22 -p 9090:9090 -d tduchateau/dandelion-sources:0.10.0
````

Once the container launched, you can connect to it in SSH:

````
ssh -p 4023 dandelion@localhost
````

Move to the `dandelion-samples` folder, then to any of the available sample:

````
cd dandelion-samples/[sample]
````

And run it:

````
mvn tomcat7:run
````

On your host machine, you should be able to access the running application at http://localhost:9090/[sample]