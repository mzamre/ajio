pipeline {
	agent any 
	parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh 'home/dev/Downloads/Mavenprac/WebApp/ajio/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/ajio.war /home/dev/Downloads/apache-tomcat-9.0.82/webapps'
			}}	
}}
