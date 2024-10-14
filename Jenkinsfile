pipeline {
    agent any
    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore SeleniumIde.sln'
            }
        }
        stage('Build') {
            steps {
                bat 'dotnet build SeleniumIde.sln --configuration Release'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test SeleniumIDE/SeleniumIde.csproj'
            }
        }
    }
}
