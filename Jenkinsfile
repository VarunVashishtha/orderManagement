pipeline {
    agent any
    
    stages {
        stage('SonarQube analysis') {
            steps
            {
                script
                {
                    def scannerHome = tool 'SonarQube Scanner 3.3'
                    withSonarQubeEnv('sonar_scanner') 
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
