# to run this image: docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=xxxx -e MYSQL_PASSWORD=xxxx web-mysql

# Derived from official mysql image (our base image)
FROM mysql
# Add a database
ENV MYSQL_DATABASE webrato
ENV MYSQL_USER myuser

# Add the content of the sql-scripts/ directory to your image
# All scripts in docker-entrypoint-initdb.d/ are automatically
# executed during container startup
COPY ./initialise.sql /docker-entrypoint-initdb.d/