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
                sh '/opt/maven/bin/mvn -f java-sample-app/pom.xml clean install' 
            }
        }
    }
}
