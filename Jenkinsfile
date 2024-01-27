pipeline {
    agent any
    
    environment {
        DOTNET_SDK_VERSION = "3.1" // Change this to your desired .NET Core SDK version
        DOTNET_RUNTIME_VERSION = "3.1" // Change this to your desired .NET Core runtime version
        SOLUTION_FILE = "notnet cidd.sln" // Change this to your solution file name
        PROJECT_NAME = "notnet cidd.csproj" // Change this to your web application project file name
        PUBLISH_DIR = "publish" // Change this to your desired publish directory name
        ARTIFACT_NAME = "YourWebApp.zip" // Change this to your desired artifact name
    }
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/pradiptakayal/.netcore.git'
                
            }
        }
        
        stage('Restore') {
            steps {
                // Restore dependencies
                sh "dotnet restore ${SOLUTION_FILE}"
            }
        }
        
        stage('Build') {
            steps {
                // Build the solution
                sh "dotnet build ${SOLUTION_FILE} --configuration Release"
            }
        }
        
       
        
       
   
    }
}
