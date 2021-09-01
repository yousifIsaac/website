pipeline {
    agent any
    stages {
        stage('Checkout from Github'){
            steps{
            git branch: 'main', credentialsId: 'token-for-website', url: 'https://github.com/yousifIsaac/website.git'''
            }
        }
        stage ('Build') {
        steps{
            echo 'Build App'
             }
        }
        stage ('Test') {
        steps{
            echo 'Test App'
             }
        }
        stage ('Release') {
        steps{
            echo 'Release App'
             }
        }
        stage ('Depoly') {
        steps{
            echo 'Deploy App'
             }
        }
    }
}
