pipeline {

    agent any

    stages{
        stage('Cloning the repository'){
            steps {
            cloneRepository()
            }
        }

        stage('Build Docker Image'){
            steps {
            sh("ls")
            sh(" echo \"Entering Build Docker Image\" ")
            }
        }

        stage('Push Docker Image'){
            steps {
            sh("echo \"Entering Docker Image push stage\"")
            }
        }

        stage('Create a sample pod'){
            steps {
            sh("echo \"Deploying a sample pod\"")
            }
        }
    }



}

def cloneRepository() {
    checkout scmGit(
            branches: [[name: 'main']],
            userRemoteConfigs: [[url: 'git@github.com:burhanshaikh/mycakeshop.git',
            credentialsId: 'mygithubkey']])
}