pipeline {

    agent {
        label 'cartforge-agent'
    }

    stages {

        stage('Clone Source Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/vrundakoli2003-sys/CartForge-Jenkins-Project.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build Application') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Package Application') {
            steps {
                sh 'tar -czf cartforge-application.tar.gz app.js package.json dist/'
            }
        }

        stage('Deliver Artifact') {
            steps {
                archiveArtifacts artifacts: 'cartforge-application.tar.gz',
                                 fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'CartForge Pipeline completed successfully!'
        }

        failure {
            echo 'CartForge Pipeline failed. Check the Console Output.'
        }
    }
}
