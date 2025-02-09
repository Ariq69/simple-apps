pipeline {
    // job akan dijalankan pada agent devops1-ariq
    agent {
        node {
            label 'devops1-ariq'
        }
    }

    // proses sdlc
    stages {
        // proses build apps
        stage('Build Apps') {
            steps {
                echo 'Build Apps'
            }
        }
        stage('Testing Apps') {
            steps {
                echo 'Testing Apps'
            }
        }
        stage('Scanning Apps') {
            steps {
                echo 'Scanning Apps'
            }
        }
        stage('Build images') {
            steps {
                echo 'Build images'
            }
        }
        stage('Deploy Apps') {
            steps {
                echo 'Deploy Apps'
            }
        }
        stage('Publish image') {
            steps {
                echo 'Publish image'
            }
        }
    }
}