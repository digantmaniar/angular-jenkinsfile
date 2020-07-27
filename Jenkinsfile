pipeline {
	agent any
	tools {
        maven 'maven-3.6.3' 
    }
	stages {
		
		stage('Checkout Source') {
			steps {
				echo 'Check out the project'
				checkout scm  
				}
			}
		
		stage('NPM Install') {
			steps {			
				echo 'NPM Install Stage start :'
			    bat "npm install"				  
				}
			}
		stage('lnit') {
			steps {	
				echo 'init Stage start :'	
                sh 'npm run lint'
				}
			}
		stage('Build') {
			steps {	
				echo 'Build Stage start :'	
                sh 'npm run build'
				}
			}
		}
	}
