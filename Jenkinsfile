pipeline {
    agent any

    stages {
        stage('Verify the code') {
            steps {
                sh 'arduino --verbose --verify --board arduino:avr:pro *.ino; done'
            }
        }
        stage('Upload') {
            steps {
                sh 'arduino --verbose --upload --board arduino:avr:pro --port /dev/ttyUSB0 *.ino; done'
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
