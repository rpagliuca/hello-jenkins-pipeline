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
            milestone()
            agent none
            steps {
                input "Deploy to prod?"
            }
        }
        stage('Deploy') {
            milestone()
            agent { docker { image 'php' } }
            steps {
                echo 'Deploying....'
            }
        }
    }

}
