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
        stage('Package') {
            steps {
                echo "Packaging.."
                sh '''
                chmod +x gradlew
                ./gradlew quarkusBuild
                '''
            }
        }
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                docker build -f src/main/docker/Dockerfile.jvm -t quarkus/hello-world-jvm .
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
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
