#!groovy
stage('Prod') {
   node() {
       
      sh '''
      
      git clone https://github.com/kulisingh/devops-test.git
      
      cd devops-test
      
      ./deploy.sh eu-west-1 ECS-Example
      
      cd ..
      
      '''
      
      deleteDir()
   }
}   
