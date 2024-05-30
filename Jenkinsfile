pipeline{
    tools{        
        maven 'my_maven'
        jdk 'my_jdk'
    }
    agent none
      stages{
          stage('Checkout'){
              agent any
              steps{
              script {
                    git branch: 'main',                        
                        url: 'https://github.com/nelavigi/NuveproRepo.git'
                }
              }
          }
          stage('Compile'){
              agent any
              steps{
                  bat 'mvn compile'
              }
          }
          stage('UnitTest'){
              agent any
              steps{                  
                  bat 'mvn test'
              }              
          }          
          stage('Package'){
              agent any
              steps{
                  bat 'mvn package'
              }
          }
      }
}
