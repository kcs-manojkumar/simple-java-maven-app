pipeline {
    agent {
        docker {
            image 'maven:3.9.0-eclipse-temurin-11' 
            args '-v /root/.m2:/root/.m2' 
            args '-v C:/ProgramData/Jenkins/.jenkins/workspace/simple-java-maven-app/:D:/manoj/Learning/jenkins/GitHub/simple-java-maven-app/'
            }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}