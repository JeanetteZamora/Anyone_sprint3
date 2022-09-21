# Sprint3
-Credit Risk Analysis-

## Objectives of the project

In this project, you will tackle one of the most common problems businesses use ML to solve: Credit Risk Analysis.

## Install

You can use `Docker` to easily install all the needed packages and libraries:

```bash
$ docker build -t sprint3 -f Dockerfile .
```

### Run Docker 

```bash
$ docker run --rm -it -p 8888:8888 -v $(pwd):/home/app/src sprint3 bash 
```

## Run Project

It doesn't matter if you are inside or outside a Docker container, in order to execute the project you need to launch a Jupyter notebook server running:

```bash
$ jupyter notebook --ip 0.0.0.0 --port 8888 --allow-root
```

Then, inside the file `AnyoneAI_Project3.ipynb`, you can see the project statement, description and also which parts of the code you must complete in order to solve it.