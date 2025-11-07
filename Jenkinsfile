pipeline {
    agent { label 'docker-agent-alpine' }

    triggers {
        pollSCM('*/5 * * * *')
    }

    stages {
        stage('Hello') {
        echo "Hello Rohin 👋 — your agent is working fine!"
           }
        }
    
        stage('Build') {
            steps {
                echo "Building..."
                sh '''
                    echo "doing build stuff..."
                '''
            }
        }

        stage('Test') {
            steps {
                echo "Testing..."
                sh '''
                    echo "doing test stuff..."
                '''
            }
        }

        stage('Deliver') {
            steps {
                echo "Delivering..."
                sh '''
                    echo "doing delivery stuff..."
                '''
            }
        }
    }
}
