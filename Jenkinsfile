pipeline{
	agent any
	tools{
		maven 'maven3.9'
	}
	stages{
		stage("Checkout_Code"){
		steps{
			git branch: 'master' , url: 'https://github.com/Biswal1997/Java_APP.git'
		     }
		}	 
		stage("Build_Code"){
		steps{
			sh 'mvn clean package'
		     }
		}
		stage("Deployment"){
		steps{
			deploy adapters: [tomcat9(credentialsId: 'tomcatcred',url: 'http://13.201.59.128:8080/')],contextPath: 'welcomeapp',war: '**/*.war'
		     }
		}
	
	}
}
