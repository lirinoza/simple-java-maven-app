pipeline {
    agent {
        docker {
            label 'windows'
            image 'mcr.microsoft.com/powershell'
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }

   }
    stages {
        stage('Build') { 
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        }
    }
}