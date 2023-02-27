FROM elliotcm/java7:1.7.0u45
MAINTAINER Elliot Crosby-McCullough "elliot@smart-casual.com"

RUN apt-get install unzip
ADD http://www.creeperrepo.net/direct/FTB2/18606e7928709218bd2a4386fb84ada9/modpacks%5EUnleashed%5E1_1_3%5EUnleashed-server.zip minecraft-ftb-unleashed.zip
RUN unzip minecraft-ftb-unleashed.zip -d /var/minecraft
RUN rm minecraft-ftb-unleashed.zip

RUN useradd -r -s /bin/false minecraft
RUN chown -R minecraft:minecraft /var/minecraft

WORKDIR /var/minecraft
ENTRYPOINT ["java", "-jar", "ftbserver.jar"]
USER minecraft

CMD ["-XX:PermSize=128m"]

EXPOSE 25565
