pipeline {

  agent any
  
   stages {

   stage('Checkout') {
      steps {
        checkout scm
        
      }
    }
     stage('verficiation'){
       steps {
  withCredentials([sshUserPrivateKey(credentialsId: '0e970807-831f-4d01-bcbb-11119d0732a2']) {
    // some block
}
     }
    stage('Ping') {
      steps {
          
          sh 'ansible all -m ping'
          
      }      
    }

  } 

}
