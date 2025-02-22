pipeline {
    agent any

    environment {
        DOTNET_VERSION = "6.0.x"
        
    }

    stages {
        stage('Restore Dependencies') {
            steps {
                sh '/usr/local/bin/dotnet/dotnet restore'
            }
        }

        stage('Build') {
            steps {
                sh '/usr/local/bin/dotnet/dotnet build --no-restore'
            }
        }

        stage('Run Tests') {
            steps {
                sh '/usr/local/bin/dotnet/dotnet test  --no-build --verbosity normal'
            }
        }
    }
}
