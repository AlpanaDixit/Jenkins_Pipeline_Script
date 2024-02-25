pipeline {
	agent any 
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/alpana/Documents/DevOpsSoftware/apache-maven-3.9.6-bin/apache-maven-3.9.6/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/Jenkins_Pipeline_Script.war /home/alpana/Documents/DevOpsSoftware/apache-tomcat-9.0.85/webapps'
			}}
		stage('slack-notification'){
		steps{	
		slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#devops', color: 'good', message: 'This is for testing', teamDomain: 'Student', tokenCredentialId: 'slacktest'	
		}}	
}}




slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#devops', color: 'good', message: 'This is for testing', teamDomain: 'Student', tokenCredentialId: 'slacktest'
