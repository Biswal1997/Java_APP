pipeline{
	agent any
	stages{
		stage('Checkout_Code'){
			steps{
				git branch: 'master',url: 'https://github.com/Biswal1997/Java_APP.git'
		    }
		}
		stage('Build_Code'){
			steps{
				sh 'mvn clean package'
		    }
		}
	}
}