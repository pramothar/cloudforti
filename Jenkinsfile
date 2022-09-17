pipeline {
    agent any
	environment {
	    PATH = "/usr/share/maven/bin:$PATH"
	}
	stages {
	    stage("clone") {
			steps{
				git credentialsId: 'git_credentials', url: 'https://github.com/pramothar/cloudforti.git'
			}
		}
		stage("build code") {
			steps {
				sh "mvn clean install"
			}
		}
		
		