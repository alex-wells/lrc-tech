# runs Carolina inside a container, also imports the team logo, fullscreen and sponsor banner image folders,
# as well as the fullscreen videos folder

# import the JDK to run Carolina
FROM openjdk AS Carolina

# copy the CRG source into the image
ADD crg /opt/crg

# set the path exports for the logos and videos
VOLUME [ "/opt/crg/html/images/fullscreen", "/opt/crg/html/images/sponsor_banner", "/opt/crg/html/images/teamlogo", "/opt/crg/html/videos/fullscreen" ]

# set the image entrypoint
ENTRYPOINT 

