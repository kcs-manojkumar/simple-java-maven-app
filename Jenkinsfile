pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v %homepath%/.m2:/root/.m2'
           	args '-e pwd=D:/manoj/Learning/jenkins/GitHub/simple-java-maven-app'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}
