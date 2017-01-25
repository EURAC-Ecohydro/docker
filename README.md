# Supported tags and respective ```Dockerfile``` links
* (Triest) *[```2.1.0```, (2.1/Dockerfile)][]*

# What is GEOtop?

GEOtop is a distributed model which numerically integrates mass and energy balances of the hydrological cycle. It is mostly used for continuum simulations in small catchments. GEOtop treats the topografical effects as a variable on the interaction between energy balance and hydrological cycle. The whole problem is solved with unique solutions.

> [www.geotop.org][]

![GEOtop logo](https://raw.githubusercontent.com/GrowWorkingHard/logos/master/geotop/GEOtop_200x250.jpg) 

# How to use this image

The containerized version of GEOtop runs on every machine (Windows, Mac OS X, GNU/Linux) and cloud platforms (AWS, GOOGLE). To set up the working environment follow these simple steps.

## Install Docker

Docker is required to run the containerized version of GEOtop. Install Docker following the instructions, depending on your platform:

* [GNU/Linux][] (then choose your distribution)
* [Mac OS X][]
* [Windows][]

## Download the [small_example][] dataset

Running GEOtop is pretty easy, but if you have never set up the working directory and the included dataset, please donwload the [small_example][] dataset and unpack it. In this way you can quickly try how easy is to run GEOtop now.

For further improvements, please consider to look into the [geotop_examples][] repository or into the [tests folder][] into the main GEOtop repo.

## Run GEOtop

To run GEOtop, open a terminal and change directory until you get to the [small_example][] folder
```
$ cd <path>/<to>/small_example
```

Then copy and paste the following command
```
$ docker run --rm  -v $(pwd):/work omslab/geotop:2.1
```
it will automatically download the dockerized version of GEOtop from the DockerHub (the download is required just for the very firs time) and run it. Any further time you will type this command, GEOtop will just simply start on your machine.

# Output

## Summary

Following a summary of the steps to take for installing and running GEOtop.

1. Install [Docker][]
2. Download and unpack the [small_example][] dataset
3. Open up a terminal emulator and change directory until get into the unpacked [small_example][] dataset
4. Run the GEOtop Docker image
   ```
   $ docker run --rm  -v $(pwd):/work omslab/geotop:2.1
   ```

# Supported Docker versions

# User Feedback

# Known Issues

## Bibliography

[```2.1.0```, (2.1/Dockerfile)]: https://github.com/geotopmodel/docker/blob/master/2.1/Dockerfile
[www.geotop.org]: http://geotopmodel.github.io/geotop/
[GNU/Linux]: https://docs.docker.com/engine/installation/
[Mac OS X]: https://docs.docker.com/docker-for-mac/
[Windows]: https://docs.docker.com/docker-for-windows/
[small_example]: https://github.com/geotopmodel/docker/blob/master/small_example.tar.gz?raw=true
[geotop_examples]: https://github.com/geotopmodel/geotop_examples
[tests folder]: https://github.com/geotopmodel/geotop/tree/master/tests
[Docker]: https://www.docker.com/