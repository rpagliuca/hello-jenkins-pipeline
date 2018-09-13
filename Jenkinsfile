pipeline {
    agent none
    stages {
        stage('Build') {
            lock('hello-jenkins-build-stage')
            agent { docker { image 'php' } }
            steps {
                echo 'Building... ?'
            }
        }
        stage('Test') {
            lock('hello-jenkins-test-stage')
            agent { docker { image 'php' } }
            steps {
                echo 'Testing... ?'
            }
        }
        stage('DeployApproval') {
            lock('hello-jenkins-deploy-approval')
            agent none
            steps {
                input "Deploy to prod?"
            }
        }
        stage('Deploy') {
            lock('deploy')
            agent { docker { image 'php' } }
            steps {
                echo 'Deploying....'
            }
        }
    }

}
