pipeline {
    agent {
        label 'maven'
    }
    stages {
        stage('SonarQube Analyzer') {
            steps {
                script {
                    def scannerHome = tool 'SonarQube Scanner 3.1';
                    withSonarQubeEnv('sonarqube') {
                        sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
                    }
                }
            }
        }
    }

}
