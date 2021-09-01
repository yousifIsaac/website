pipeline {
    agent any
    stages {
        stage ('Chekout from SCM') {
        steps {
                git branch: 'main', credentialsId: 'yousifishaag', url: 'https://github.com/yousifIsaac/website.git'
            }
        }
        stage ('Build') {
        steps{
            echo 'Build App'
             }
        }
    }
}
