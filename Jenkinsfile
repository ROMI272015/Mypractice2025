pipeline {
    agent any

    triggers {
        pollSCM('*/1 * * * *')
    }

    stages {
       stage('Build') {
            steps {
                echo "Building..."
                sh '''
                    pip install -r requirement.txt
                    echo "doing build stuff..."
                '''
            }
        }

        stage('Test') {
            steps {
                echo "Testing..."
                sh '''
                    python3 hello.py
                    python3 hello.py --name=Brad
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
