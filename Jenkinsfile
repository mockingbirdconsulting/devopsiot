pipeline {
    agent any

    stages {
        stage('Verify the code') {
            steps {
                sh 'for b in $(cat boards.txt); do arduino --verify --board $(echo $b|cut -d ";" -f 1) *.ino; done'
            }
        }
        stage('Upload') {
            steps {
                sh 'for b in $(cat boards.txt); do arduino --upload --board $(echo $b|cut -d ";" -f 1) --port $(echo $b|cut -d ";" -f 2) *.ino; done'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
