#!groovy
node() {
   stage('Test') {
    
      deleteDir()
       
      sh '''

      set -e
      
      git clone https://github.com/kulisingh/devops-test
      
      cd devops-test/services/api
      npm test
      
      cd ../..
      
      '''
      
   }
   stage('Prod') {
       
      sh '''
      
      set =e
      
      cd devops-test
      
      ./deploy.sh eu-west-1 ECS-Example
      
      cd ..
      
      '''
      
      deleteDir()
   }   
}   
A

