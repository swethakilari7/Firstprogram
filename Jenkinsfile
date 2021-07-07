//node {
  /* Requires the Docker Pipeline plugin to be installed */
  //docker.image('node:7-alpine').inside {
  //stage('Test') {
    //sh 'node --version'
 // }
  //}
//}
pipeline {
    agent { dockerfile true }
        
    stages {
        stage('Example') {
            steps {
                echo "creating Dockerfile"
                echo "FROM node:7-alpine:latest" > Dockerfile
                docker build -t dockerimage -f Dockerfile .
                sh 'node --version'
                //sh 'svn --version'
            }
        }
    }
}
