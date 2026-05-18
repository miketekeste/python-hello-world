pipeline {
    agent { 
        node {
            label 'Docker-Agent-python'
            }
      }
      triggers {
        pollSCM 'H/5 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd MyApp
                pip install --break-system-packages -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing..TESdena neh endet neh"
                sh '''
                cd MyApp
                python3 hello.py
                python3 hello.py --name=Brad
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
