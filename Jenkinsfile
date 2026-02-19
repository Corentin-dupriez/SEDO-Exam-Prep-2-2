pipeline {
    agent any 

    stages{ 
      stage("restore dependencies"){
          when { branch 'main'}
          steps{
              sh 'dotnet restore'
            }
        }
      stage("build the app"){
        when { branch 'main'}
         steps{
              sh 'dotnet build --no-restore'
            }
        }
      stage("run the tests"){
        when { branch 'main'}
        steps{
              sh 'dotnet test'
            }
        }
  }
}
