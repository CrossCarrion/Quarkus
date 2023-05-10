pipeline {
    
    environment {
        dockerimagename = "crosscarrion/quarkus-app"
        dockerImage = ""
    }
    agent { 
        node {
            label 'docker-agent-alpine'
            }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                man docker build
                docker build -f src/main/docker/Dockerfile.jvm -t quarkus/hello-world-jvm
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff..
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
