pipeline{
    agent any
    
    
     stages{
        stage("Restore code"){
           when {
                branch 'main'
            }
            steps{
                echo "Restoring code"
                bat "dotnet restore"
            }

            
            
        }
        stage("Building code"){
            when {
                branch 'main'
            }
            steps{
                echo "Building code"
                bat "dotnet build --no-restore"
            }
        }
        stage("Test code"){
            when {
                branch 'main'
            }
            steps{
                echo "Testing code"
                bat "dotnet test --no-build"
            }
        }
  }
    
}
