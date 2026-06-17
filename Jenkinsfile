pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	stages{
		stage('Checkout')
		{
		steps{
			git branch 'main' , url:'https://github.com/Darshan429/gradle.git'
		}
		}
		stage('Build')
		{
		steps{
			sh 'gradle build'
		}
		}
		stage('Test')
		{
		steps{
			sh 'gradle test'
		}
		}
		stage('Run Application')
		{
		steps{
			sh 'gradle run'
		}
		}
	}
	
	post{
		success{
			echo 'Build and Deployment successfull'
		}
		failure{
			echo 'Build Failure'
		}
	}
}
