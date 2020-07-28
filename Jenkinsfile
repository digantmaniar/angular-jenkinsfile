pipeline {
	agent any
	//tools {
       // maven 'maven-3.6.3' 
        //    }
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
                         bat "npm run lint"
				}
			}
		stage('Build') {
			steps {	
				echo 'Build Stage start :'	
                bat "npm run build"
				}
			}
		}
	}
