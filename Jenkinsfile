pipeline {
    agent {
        docker {
            image 'maven:maven_3_5_0'
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