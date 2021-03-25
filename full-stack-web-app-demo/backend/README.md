Hopefully, the comments on each line explain what's going on.

There is one big difference between the frontend- and the backend-dockerfile. The former contains code to build the application. If we make changes to the backend, we will need to build it first using this command.

gradle build

on mac 

sh gradlew build

To build the image we simply execute this command on the terminal. Again, make sure to run it from your projects root directory!

docker build --file=backend/backend.dockerfile  -t playground-web-backend .
—file → The file to use for the build
-t → To identify our image we tag it
. → The location of the build context (the app). In our case the current directory, referenced as .