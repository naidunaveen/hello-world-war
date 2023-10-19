pipeline {
   agent {
	 label 'slave5'
            }
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
	      stage('tomcat installation') {
            steps {		
		sh 'sh automation.sh'
		    echo "tomcat installed"
	    }
	}
        stage('deploy') {
            steps {
		    echo "good"
	            sh 'sudo cp /home/ubuntu/workspace/assignmentpipe/target/hello-world-war-3.0.0.war /var/lib/tomcat9/webapps'//
            }
        }    
    }
}
	    
    
