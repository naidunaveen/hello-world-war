pipeline {
    agent none
      stages {
        stage('checkout') {
	    agent {
	     label 'slave4'
            }
            steps {
		sh 'rm -rf hello-world-war'    
		sh 'git clone https://github.com/naidunaveen/hello-world-war/'
            }
        }
	stage('Build') {
	    agent {
	    label 'slave4'
            }
            steps {		
		sh 'mvn clean package'
	    }
	}
        stage('deploy') {
	     agent {
	     label 'slave3'
            }
            steps {
		    echo "good "
	            // sh 'sudo cp /var/lib/jenkins/workspace/multibranch_pipeline1_develop/target/hello-world-war-3.0.0.war /var/lib/tomcat9/webapps'//
            }
        }    
    }
}
	    
    
