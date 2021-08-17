pipeline {
    agent {
        label 'docker-slave-demo'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
