#!groovy

properties([disableConcurrentBuilds()])

pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
        timestamps()
    }
    stages {
        stage("Build images") {
            steps {
                sh 'docker build -t my-swagger-ui .'
            }
        }

        stage("Run images") {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
