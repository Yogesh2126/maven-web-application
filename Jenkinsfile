
pipeline {
        agent any
	            tools {
		               maven 'maven'
	                 }

	     stages {
		         stage (' maven compile') {
				     steps {
					       sh 'mvn compile'
						}
				    }
		         stage ('test') {
				        steps {
						   sh 'mvn test'
						}
					}	
			 stage ('clean package') {
				     steps {
					     sh 'mvn clean package'
					 }
				}
		          stage ('deploy') {
				  steps {
				     sh 'cp -r /var/lib/jenkins/workspace/maven-project/target/maven-web-application.war /mnt/apache-tomcat-9.0.98/webapps'
				    }
				}
		   }
 }
