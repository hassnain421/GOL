node {
  stage('SCM') {
    git 'https://github.com/hassnain421/GOL.git'
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar"
    }
  }
}
