
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
		   }
 }
