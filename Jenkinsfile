pipeline {
    agent {
        docker {
            image 'maven:3.9.0-eclipse-temurin-11' 
            args '-v  %homepath%/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
            	dir(path: 'D:/manoj/Learning/jenkins/GitHub/simple-java-maven-app') {
                sh 'mvn -B -DskipTests clean package' 
                }
            }
        }
    }
}