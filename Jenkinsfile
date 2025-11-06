pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/nafisakhan05/jenkinsdemo3.git'
            }
        }

        stage('Extract Data') {
            steps {
                bat 'python extract.py'
            }
        }

        stage('Transform Data') {
            steps {
                bat 'python transform.py'
            }
        }

        stage('Load Data') {
            steps {
                bat 'python load.py'
            }
        }

    }
}
