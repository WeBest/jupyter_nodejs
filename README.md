[![Docker Stars](https://img.shields.io/docker/stars/jessewei/jupyter_nodejs.svg?style=flat-square)](https://hub.docker.com/r/jessewei/jupyter_nodejs/)
[![Docker Pulls](https://img.shields.io/docker/pulls/jessewei/jupyter_nodejs.svg?style=flat-square)](https://hub.docker.com/r/jessewei/jupyter_nodejs/)

# Jupyter with multiple engine support 
This repository is a Jupyter service for data science.

It covered many programing language kernel, IPython3 (python2.7.9), IJulia, IRkernel, IGo, IScala, Bash, Redis kernel, IJavascript.
Distribution of python is anaconda-2.1.0, this distribution is the latest version of using python2. 

Those utilites included for [IBM Watson service](https://console.ng.bluemix.net/) laboratory are listed as below:
- Google Cloud API
- Watson SDK for nodejs and python
- Node.js: json-query
- Python: wordcloud

## Docker Hub Description
### Docker Installation

- [Windows](https://docs.docker.com/windows/step_one/),  [MacOS](https://docs.docker.com/mac/step_one/), [Linux](https://docs.docker.com/linux/step_one/)

### Run

1. Run by name
Attach volumne for saving notebook in host OS.
``` 
$ docker run --name nb -d -v /c/Users/yourName/workspace:/notebooks/workspace -p 8889:8888  jessewei/jupyter_nodejs
```
``` 
    --name <container name>
    -v <work-directory on host machine>:/notebooks/workspace
```     

2. Start/Stop/Remove container    
``` 
$ docker start nb
$ docker stop nb
$ docker rm nb    
```

3. Access container 
``` 
$ docker exec -it nb bash
```


### Open broswer and Go to:
``` 
http://192.168.99.100:8889/
``` 

- The 192.168.99.100 is default docker machine ip, you may like to verify by

```
$ docker-machine ip
``` 



## Docker Cloud Description
This images also managed by cloud.docker, and run on Softlayer.

### Open broswer and Go to:
``` 
http://notebook.jessewei.tk:8889
``` 



## Sample notebooks
### Notebook location
``` 
http://192.168.99.100:8889/tree/nb_demo/watson
``` 
### Notebook list
The notebook naming start from api and kernel used.
- **alchemy_language-py.ipynb**, alchemy_language API in python sample
- **alchemy_vision-py.ipynb**, alchemy_vision API in python sample
- **google_vision-py.ipynb**, Google vision API in python sample


