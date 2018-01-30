# runs Carolina inside a container, also imports the team logo, fullscreen and sponsor banner image folders,
# as well as the fullscreen videos folder

# import the JDK to run Carolina
FROM openjdk

# set the working directory
WORKDIR /crg

# copy the CRG source into the image
ADD . /crg

EXPOSE 8000

# set the path exports for the logos and videos
VOLUME [ "/crg/html/images/fullscreen", "/crg/html/images/sponsor_banner", "/crg/html/images/teamlogo", "/crg/html/videos/fullscreen" ]

# set the startup command
CMD ["/crg/scoreboard-Linux.sh"]

