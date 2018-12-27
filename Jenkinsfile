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
                sh '${m2_home}/opt/maven -f java-sample-app/pom.xml clean install' 
            }
        }
    }
}
