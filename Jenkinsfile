pipeline {
    agent any

    stages {
        stage('Verify the code') {
            steps {
                sh 'arduino --verbose --verify --board arduino:avr:pro *.ino'
            }
        }
        stage('Upload') {
            steps {
                sh 'arduino --verbose --upload --board arduino:avr:pro --port /dev/ttyUSB0 *.ino'
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
