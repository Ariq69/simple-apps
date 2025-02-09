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
                // echo 'Build Apps'
                sh 'npm install'
            }
        }
        stage('Copy env') {
            steps {
                // echo 'Testing Apps'
                sh 'cp -p /home/ubuntu/Hari-1/simple-apps/.env .'
            }
        }
        stage('Testing Apps') {
            steps {
                // echo 'Testing Apps'
                sh 'npm test'
            }
        }
        stage('Scanning Apps') {
            steps {
                // echo 'Scanning Apps'
                sh 'sonar-scanner   -Dsonar.projectKey=simple-apps   -Dsonar.sources=.   -Dsonar.host.url=http://172.23.5.13:9000   -Dsonar.login=sqp_68169ea03ab10c79ddac585dbf1dc02688978036'
            }
        }
        stage('Build images') {
            steps {
                // echo 'Build images'
                sh 'docker compose build'
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