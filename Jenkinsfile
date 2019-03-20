pipeline {
    agent any
    tools {
        scannerHome = tool 'SonarQube Scanner 3.3'
    }
    stages {
        stage('SonarQube analysis') {
            steps
            {
    withSonarQubeEnv('sonar_scanner') {
      sh "${scannerHome}/bin/sonar-scanner"
    }
            }
  }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
