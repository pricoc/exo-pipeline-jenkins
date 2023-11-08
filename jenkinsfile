pipeline {
    agent any

    stages {
        stage('Checkout Git') {
            steps {
                echo 'Checkout Git into Jenkins workspace'
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/pricoc/exo-pipeline-jenkins.git'
            }
        }
        stage('Build') {
            steps {
                echo 'now this is the build stage'
                bat 'build.bat'
            }
        }
        stage('Unit') {
            steps {
                echo 'now this is the unitary test stage'
                bat 'unit.bat'
            }
        }
        stage('Deploy') {
            steps {
                echo 'now this is the deployment stage'
                bat 'deploy.bat'
            }
        }
    }
}
