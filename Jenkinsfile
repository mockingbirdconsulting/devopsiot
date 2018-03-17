pipeline {
    agent any

    stages {
        stage('Verify the code') {
            steps {
                shell "for b in $(cat boards.txt); do arduino --verify --board $b *.ino; done"
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
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
