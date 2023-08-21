# Installation
In this file, we provide instructions on how to build the docker container, which contain the necessary data and code to reproduce our experimental results.

## Prerequisites

 - Install Docker from the official website[^fn1]
 
 [^fn1]: https://docs.docker.com/desktop/install/windows-install/.

## Start Docker 
After Docker is installed,  change the working directory to `docker` folder in the repository with:

`cd docker`

Start the docker container with the following command:

`docker-compose up`

You should see the following output.

[![Supervised](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")

By now, you should be able to see a running docker container named `docker` in your docker desktop. 

[![Supervised](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")](https://github.com/BonanKou/decide/blob/main/image/docker_one.png "Supervised")

The `docker` container should contain two separate docker containers (`myneo4j` and `decide`). Proceed to the terminal of `decide`:

[![Supervised](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")

Now, you can run DECIDE and reproduce all our experimental results following the instructions from the README file. For example, try running:

`python3 main.py -n CFL -m file`

You should see the following output:

[![Supervised](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")](https://github.com/BonanKou/ASSORT-Automatic-Summarization-of-Stack-Overflow-Posts/blob/main/screenshots/supervised.png "Supervised")
