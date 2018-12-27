pipeline {
	agent { label 'ansible' }
    stages {
        stage ('checkout') {
            steps {
		checkout scm
            }
        }
        stage ('Build') {
            steps {
                sh '${M2_HOME}/bin/mvn -f java-sample-app/pom.xml clean install' 
            }
        }
    }
}
