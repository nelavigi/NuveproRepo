pipeline{
    tools{        
        maven 'MAVEN_HOME'
    }
    agent none
      stages{
          stage('Checkout'){
              agent any
              steps{
              git 'https://github.com/nelavigi/NuveproRepo.git'
              }
          }
          stage('Compile'){
              agent any
              steps{
                  sh 'mvn compile'
              }
          }
          stage('UnitTest'){
              agent any
              steps{
                  git 'https://github.com/nelavigi/NuveproRepo.git'
                  sh 'mvn test'
              }              
          }          
          stage('Package'){
              agent any
              steps{
                  sh 'mvn package'
              }
          }
      }
}
