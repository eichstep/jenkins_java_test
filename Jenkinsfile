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
		sh './script/deliver.sh'
	    }
	}
    }
}
