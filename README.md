# docker-multibuild-example
This is an demonstration project for dockerfile and dockerfile multi stage build concept

Clone the project from git and follow below steps
git clone https://github.com/jaintpharsha/multi_stage.git

Creating container with normal Dockerfile

	"STEP 1: Building nodewebapp from Dockerfile_normal"
		docker build -t nodewebapp:v1 -f Dockerfile_normal .

	"STEP 2: Creating Conatiner Out of Image"
		docker run -it -d -p 8081:8085 nodewebapp:v1

Creating container with multi-stage Dockerfile

	"STEP 1: Building nodewebapp from Dockerfile_normal"
		docker build -t nodewebappmulti:v1 -f Dockerfile_multistage .

	"STEP 2: Creating Conatiner Out of Image"
		docker run -it -d -p 8082:8085 nodewebappmulti:v1

