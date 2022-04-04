FROM ubuntu:18.04 
MAINTAINER "Tyson Lee Swetnam" tswetnam@cyverse.org 
RUN apt-get update && apt-get install -y fortune cowsay lolcat 
ENV PATH=/usr/games:${PATH} 
ENV LC_ALL=C
ENTRYPOINT fortune | cowsay | lolcat
