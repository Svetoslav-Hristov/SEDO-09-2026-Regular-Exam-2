pipeline{
    agent any
    
    
     stages{
        stage("Restore code"){
           
            steps{
                echo "Restoring code"
                bat "dotnet restore"
            }

            
            
        }
        stage("Building code"){
            
            steps{
                echo "Building code"
                bat "dotnet build --no-restore"
            }
        }
        stage("Test code"){
            
            steps{
                echo "Testing code"
                bat "dotnet test --no-build --verbosity normal"
            }
        }
  }
    
}
