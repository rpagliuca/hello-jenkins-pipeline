pipeline {

    agent {
        docker {
            image 'php'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building... ?'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy approval') {
            input "Deploy to prod?"
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

}
