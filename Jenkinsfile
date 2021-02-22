pipeline {
    agent {
        docker {
            image 'maven:3.6.0-jdk-13' 
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