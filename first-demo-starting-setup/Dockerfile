# use node.js as base image 
FROM node:14  
# specify special directory you wanna work in. 
WORKDIR /app 
# copy package.json into the working directory 
COPY package.json . 
# run the npm command to install dependencies specified in package.json
RUN npm install 
# copy rest of the code files within dir into the WORKDIR
COPY . . 
# expose port to outside world (app.mjs specified port 3000)
EXPOSE 3000
# execute '$ node app.mjs' command 
CMD ["node", "app.mjs"]



# run '$ docker build .' in this directory. 
    # builds an image based on this Dockerfile
    # grabs node environment (node:14) and rest of instructions
    # results in image that is ready to be started as a container
    # notice the logs has image sha: 
        # ex:  => => writing image
        # sha256:ccb00fc617f1abd99fc456db5d7324dfc7f1f2a518a499b82bd59e6a2dac619f
        # docker run <image_id> 
        # if port: docker run -p 3000:3000 <image_id>
    
    # docker ps to see list of containeres 
    # docker stop <name/image_id> to stop the container 