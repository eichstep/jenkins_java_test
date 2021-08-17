pipeline {
    agent {
        label 'docker-slave-demo'
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
