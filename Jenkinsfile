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
                sh '${m2_home}/etc/alternatives/mvn -f java-sample-app/pom.xml clean install' 
            }
        }
    }
}
