# instructions for setting up the image.
FROM node

# run subsequent commands inside /app
WORKDIR /app

# which files from local should go into image
# first dot (current local dir)
# second dot defaults to working directory. - default is /root if not set.
# /folder (host folder) - creates folder if doesnt exist
COPY . /app

RUN npm install 

# expose port 80 (whatever port our app is running.)
EXPOSE 80

# Difference between RUN VS CMD 
# RUN: executes when image is created 
# CMD: executes when container is started.
CMD ["node", "server.js"] 