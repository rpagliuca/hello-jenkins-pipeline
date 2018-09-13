pipeline {
    agent none
    stages {
        stage('Build') {
            agent { docker { image 'php' } }
            steps {
                echo 'Building... ?'
            }
        }
        stage('Test') {
            agent { docker { image 'php' } }
            steps {
                echo 'Testing..'
            }
        }
        stage('DeployApproval') {
            agent none
            steps {
                input "Deploy to prod?"
            }
        }
        stage('Deploy') {
            agent { docker { image 'php' } }
            steps {
                echo 'Deploying....'
            }
        }
    }

}
