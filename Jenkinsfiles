node {
  stage('SCM') {
    git 'https://github.com/atoy3731/my-app.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv(credentialsId: 'sonarqube', installationName: 'Sonarqube') { // You can override the credential to be used
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
    }
  }
}
