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
                sh 'mvn clean install'
            }
        }
        stage('maven compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('maven sonar'){
            steps{
                sh 'mvn sonar:sonar -Dsonar.login=admin -Dsonar.password=sonar -Dmaven.test.skip=true'
            }
        }
        
    }
}