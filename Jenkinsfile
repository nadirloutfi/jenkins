pipeline {
    environment {
        registry = "docker_hub_account/repository_name"
        registryCredential = 'dockerhub'
    }

    agent {
        label 'docker'
    }

    stages {
        stage('Building our image') {
            steps {
                script {
                    dockerImage = docker.build "mcasperson/petclinic:$BUILD_NUMBER"
                }
            }
        }
    }
}