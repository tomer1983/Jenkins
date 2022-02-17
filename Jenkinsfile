pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                echo 'CheckIfFileExist'
                writeFile file: 'myNewFile.txt', text: 'rock you!!!'
                fileExists('file.txt') 
            }
        }        
        stage('Build') {
            steps {
                echo 'Build'
                git branch: 'main', credentialsId: 'myGitHubAccount', url: 'https://github.com/tomer1983/Jenkins.git'
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
        }
        stage('Release') {
            steps {
                echo 'Release'
            }
        }        
    }
}
