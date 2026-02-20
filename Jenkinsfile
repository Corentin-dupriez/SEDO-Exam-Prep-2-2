pipeline {
    agent any 

    stages{ 
      stage("restore dependencies"){
        when {
            expression {
                return env.GIT_BRANCH == 'origin/main'
              }
          }
          steps{
              sh 'dotnet restore'
            }
        }
      stage("build the app"){
        when {
          expression {
              return env.GIT_BRANCH == 'origin/main'
            }
        }
        steps{
              sh 'dotnet build --no-restore'
            }
        }
      stage("run the tests"){
        when {
          expression {
              return env.GIT_BRANCH == 'origin/main'
            }
        }
      steps{
              sh 'dotnet test'
            }
        }
  }
}
