pipeline {
	agent any
	parameters {
  choice choices: ['QA', 'UAT'], description: 'any', name: 'Environment'
}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/puja/Downloads/apache-maven-3.8.7/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			
			sh 'cp target/jordan.war /home/puja/Downloads/apache-tomcat-9.0.70/webapps'
	}
}}}
