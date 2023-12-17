pipeline{
	agent any
	tools{
		maven 'maven3.9'
	}
	stages{
		stage("Checkout Code"){
		steps{
			git branch: 'master' , url: 'https://github.com/chinmay1998/Java_Project.git'
		     }
		}	 
		stage("Build_Code"){
		steps{
			sh 'mvn clean package'
		     }
		}
		stage("Deployment"){
		steps{
			deploy adapters: [tomcat9(credentialsId: 'tomcatcred',url: 'http://18.61.30.53:8080/')],contextPath: 'welcomeapp',war: '**/*.war'
		     }
		}
	
	}
}