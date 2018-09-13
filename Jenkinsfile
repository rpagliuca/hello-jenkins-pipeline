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
                echo 'Testing... ?'
            }
        }
        stage('DeployApproval') {
            agent none
            steps {
                milestone()
                input "Deploy to prod?"
            }
        }
        stage('Deploy') {
            agent { docker { image 'php' } }
            steps {
                milestone()
                echo 'Deploying....'
            }
        }
    }

}
