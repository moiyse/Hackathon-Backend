pipeline {
    agent any

    stages {
        stage('GIT') {
            steps {
                echo 'Getting Project from Git'
                    git branch: 'master',
                    url : 'https://github.com/moiyse/Hackathon-Backend.git'
            }
        }
        stage('mvn clean') {
            steps{
                sh 'mvn clean'
            }
        }
        stage('maven compile'){
            steps{
                sh 'mvn package'
            }
        }
    }
}