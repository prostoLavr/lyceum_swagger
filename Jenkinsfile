#!groovy

properties([disableConcurrentBuilds()])

pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
        timestamps()
    }
    stages {
        stage("Run images") {
            steps {
                sh 'ls'
                sh 'pwd'
                sh 'docker-compose up -d'
            }
        }
    }
}
