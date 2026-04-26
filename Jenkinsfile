pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {

        stage('CHECKOUT') {
            steps {
                git 'https://github.com/vvce23ise0051-creator/cc.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}