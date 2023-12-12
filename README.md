## Automated CI/CD pipline with GitHub Actions

Code in this repository is set up for an automated CI/CD workflow, focusing on building a Java app artifact, 
creating a Docker image, and pushing it to a private DockerHub repository. Additional useful comments on CI 
configuration can be found in [`.github/workflows/ci.yml`](https://github.com/nadyinky/gha-docker-flow/blob/fb0b7fec14a785a60d086f83a270612005151d96/.github/workflows/ci.yml).

- The build artifact represents the compiled and packaged basic Java application.
- The build artifact is then used to create a Docker image. The Docker image encapsulates the Java application and its dependencies.
- The Docker image is pushed to a private DockerHub repository for secure storage and distribution.

___
##### build the project

    ./gradlew build

##### build Docker image called java-app. Execute from root

    docker build -t java-app .
    
##### push image to repo 

    docker tag java-app demo-app:java-1.0
    
