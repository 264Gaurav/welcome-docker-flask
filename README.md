# Docker: Flask Basic App

## Project Setup

1. **Install Docker**
   Ensure Docker is installed on your local system. You can download it from [Docker's official website](https://www.docker.com/).

2. **Login to Docker CLI**
   Make sure you are logged in via the Docker CLI by providing your username and password. Run the following command:

```bash
docker login
```

3. **Clone or Download the Repository**
   Clone this repository using Git or download it as a ZIP file and extract it.

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

4. **Build the Docker Image**
   Build the Docker image using the following command:

   ```bash
   docker build -t welcome-app .
   ```

5. **Run the Docker Container**
   Run the Docker container and map port 8000 of the container to port 8000 on your local machine:

   ```bash
   docker run -p 8000:8000 welcome-app
   ```

   Now, you can access the server at http://localhost:8000.

6. **Tag the Docker Image**
   Rename (tag) the Docker image to prepare it for pushing to Docker Hub:

   ```bash
   docker tag welcome-app <USER_NAME>/welcome-app:latest
   ```

7. **Push the Docker Image to Docker Hub**
   Push the Docker image to your Docker Hub account:
   ```bash
   docker push <USER_NAME>/welcome-app:latest
   ```

## Using This Project

Once the Docker image is pushed to Docker Hub, anyone can pull the image and run it to build the container on their local system.

### Steps to Use the Docker Image:

1. **Pull the Docker Image**
   Run the following command to pull the image:

```bash
docker pull <USER_NAME>/welcome-app:latest
```

2. **Run the Docker Container**
   Use the pulled image to run the container:

   ```bash
   docker run -p 8000:8000 <USER_NAME>/welcome-app:latest
   ```

## Additional Information

### Prerequisites:

Ensure Docker is installed and running on your system.
Make sure you have a Docker Hub account to push and pull images.
**Flask Application:**
This project contains a basic Flask application. You can modify the Flask app code as needed before building the Docker image.

**Docker Commands Overview:**

docker build: Builds a Docker image from the specified Dockerfile.
docker run: Runs a container from a Docker image.
docker tag: Tags an existing Docker image with a new name.
docker push: Pushes a Docker image to a remote repository (e.g., Docker Hub).
docker pull: Pulls a Docker image from a remote repository.

**Accessing the Application:**
After running the container, you can access the Flask application at http://localhost:8000.

Feel free to customize this README further based on your project's requirements! ```

<!-- # Docker: Flask basic app

## project setup

1. Install Docker in your local system
2. Make sure you are logged In via CLI by providing username and password
3. Now , clone this repo or download as zip
4. run : bash `docker build -t welcome-app .`
5. run : bash `docker run -p 8000:8000 welcome-app` . Now, you can see your server running at localhost:8000 and at port 8000 in container
6. rename the docker project : bash `docker tag welcome-app <USER_NAME>/welcome-app:latest`
7. push the docker image to docker hub : bash `docker push  <USER_NAME>/welcome-app:latest`

## Using this project :

Now anyone can just pull this docker image and run it to build the container on their own local system. -->
