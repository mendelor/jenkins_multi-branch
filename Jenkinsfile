pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "/opt/maven/bin/mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "/opt/maven/bin/mvn test"
            }
        }
        stage('--worker--') {
            steps {
                sh "/opt/maven/bin/mvn package"
            }
        }
    }
}
