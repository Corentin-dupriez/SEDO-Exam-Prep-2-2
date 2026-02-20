pipeline {
    agent any 

    stages{ 
      stage("restore dependencies"){
          steps{
              sh 'dotnet restore'
            }
        }
      stage("build the app"){
         steps{
              sh 'dotnet build --no-restore'
            }
        }
      stage("run the tests"){
        steps{
              sh 'dotnet test'
            }
        }
  }
}
