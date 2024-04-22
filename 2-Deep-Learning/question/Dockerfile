FROM ubuntu:22.04

LABEL author = "Jin"
LABEL description = "The solution of second exercise"

#easy way to get packages in ubuntu is using `apt-get`
# Install dependencies 
RUN apt-get update 
RUN apt-get upgrade -y
RUN apt-get install python3-dev python3-dev python3-pip -y 
RUN pip3 install --upgrade pip 

RUN pip3 install tensorflow==2.14.0 matplotlib==3.8.0 jupyterlab==4.0.7

# change workdirectory, good thing about this is then we dont need to specify the workdir afterward 
WORKDIR /root/notebooks

# copy this file to root, the default workdir is depending on the image 
COPY ./dream.ipynb dream.ipynb


#once we finish the build, it will execute this bash script thats in the root 
ENTRYPOINT ["/entrypoint.sh"] 