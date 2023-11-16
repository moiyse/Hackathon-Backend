pipeline {
    agent any

    stages {
        stage('GIT') {
            steps {
                echo 'Getting Project from Git'
                    git branch: 'master',
                    url : 'https://github.com/moiyse/jari-backend.git'
            }
        }
        stage('mvn clean') {
            steps{
                sh '''
                cd pfe
                mvn clean
                '''
            }
        }
        stage('maven son'){
            steps{
                sh '''
                cd pfe
                mvn package
                '''
            }
        }
    }
}