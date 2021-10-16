pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                    git branch: 'main', credentialsId: 'jenkins', url: 'git@github.com:bohdankits05/devops14-jenkins-public.git'
                }
            }

        stage ('Test') {
            steps {
                script{
                    sh "chmod +x -R ${env.WORKSPACE}/../${env.JOB_NAME}/test.sh"
                }
            }
        }
    }
}
