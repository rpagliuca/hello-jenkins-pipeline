pipeline {
    agent none
    stages {
        lock('hello-jenkins-build') {
            stage('Build') {
                agent { docker { image 'php' } }
                steps {
                    echo 'Building... ?'
                }
            }
        }
        lock('hello-jenkins-test') {
            stage('Test') {
                agent { docker { image 'php' } }
                steps {
                    echo 'Testing... ?'
                }
            }
        }
        lock('hello-jenkins-deploy-approval') {
            stage('DeployApproval') {
                agent none
                steps {
                    input "Deploy to prod?"
                }
            }
        }
        lock('hello-jenkins-deploy') {
            stage('Deploy') {
                agent { docker { image 'php' } }
                steps {
                    echo 'Deploying....'
                }
            }
        }
    }

}
