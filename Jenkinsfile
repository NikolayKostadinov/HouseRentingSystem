pipeline {
	agent any
	stages {
		stage('Restor NuGet packages') {
			steps {
				bat 'dotnet restorte'
			}
		}

		stage('BuildProject') {
			steps {
				bat 'dotnet build --no-restore'
			}
		}
		stage('Execute tests') {
			steps {
				bat 'dotnet test --no-build --verbosity normal'
			}
		}
	}
}
