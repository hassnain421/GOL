node {
  stage('Clone the Git') {
    git 'https://github.com/hassnain421/GOL.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'sonarqube';
    withSonarQubeEnv('sonarqube') {
      sh "${scannerHome}/bin/sonar-scanner \
      -D sonar.login=admin \
      -D sonar.password=1234 \
      -D sonar.projectKey=test1 \
      -D sonar.exclusions=vendor/**,resources/**,**/*.java \
      -D sonar.host.url=http://143.198.7.75:9000/"
    }
  }
}
