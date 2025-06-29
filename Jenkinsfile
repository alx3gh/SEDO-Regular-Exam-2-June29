pipeline {
	agent any
	
	stages {
		stage ('Checkout') {
			steps {
				checkout scm
			}
		}
		stage ('Restore project') {
			steps {
				bat 'dotnet restore'
			}
		}
		stage ('Build project') {
			steps {
				bat 'dotnet build --no-restore'
			}
		}
		stage ('Test project') {
			steps {
				bat 'dotnet test --no-build --verbosity normal'
			}
		}
	}
}