pipeline {
    agent any
    
    stages {
        stage('SonarQube analysis') {
            steps
            {
                script
                {
                    def scannerHome = tool 'sonar_scanner'
                    withSonarQubeEnv('sonarqube') 
                    {
                        sh "${scannerHome}/bin/sonar-scanner"
                    }
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
