node
{
    stage('clonning from GIT'){
        git 'https://github.com/hassnain421/jenkins-sonarqube.git'
     }
     stage('SonarQube Analysis') {
        
    def scannerHome = tool 'sonarqube'
      withSonarQubeEnv('sonarqube') {
      sh """/var/lib/jenkins/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonarqube/bin/sonar-scanner \
      -D sonar.projectVersion=1.0-SNAPSHOT \
      -D sonar.login=admin \
      -D sonar.password=1234 \
      -D sonar.projectBaseDir=/var/lib/jenkins/workspace/sq/ \
      -D sonar.projectKey=sonarqubetest 
      -D sonar.projectKey=test1 \
      -D sonar.sources=my-app/src/main \
      -D sonar.tests=my-app/src/test \
      -D sonar.host.url=http://143.198.7.75:9000//"""
        }
}
}
