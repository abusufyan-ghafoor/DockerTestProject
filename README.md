After cloning this repo install node js and related dependencies
then open docker and pull mongo and mongo-express from docker CLI
then run the below commands to create network and run the mongo and mongo-express with the given commands
docker network create mongo-network
 docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password  --name mongodb --net mongo-network mongo
docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password -e ME_CONFIG_MONGODB_SERVER=mongodb --net mongo-network --name mongo-express mongo-express

then open localhost:8081 to open mongo-express GUI and then create a database user-account and then create collection users 
then run localhost:3001 and update the user profile and to see the results open mong0-express GUI
