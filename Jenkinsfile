node {
  stage('Clone the Git') {
    git branch: 'main', credentialsId: 'yousifishaag', url: 'https://github.com/yousifIsaac/website.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'sonarqube';
    withSonarQubeEnv('sonarqube') {
      sh "${scannerHome}/bin/sonar-scanner \
      -D sonar.login=admin \
      -D sonar.password=slnee@123 \
      -D sonar.projectKey=sonarqube \
      -D sonar.host.url=http://192.168.1.30:9000/"
    }
  }
  stage('Quality Gates'){
    timeout(time: 1, unit: 'HOURS') {
    def qg = waitForQualityGate()
    if (qg.status != 'OK') {
      error "Pipeline aborted due to quality gate failure: ${qg.status}"
    }
    }      
  }
}

