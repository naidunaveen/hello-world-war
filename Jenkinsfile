pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {	
		sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/naidunaveen/hello-world-war/'
            }
        }
	stage('Build') {
            steps {				
                sh 'mvn clean package'
            }
        }
	stage('deploy') {
            steps {
		    sh 'sudo cp /var/lib/jenkins/workspace/multipipe1_dev/target/hello-world-war-5.0.0.war /var/lib/tomcat9/webapps'
            }
	}
    }
}
	    
    
