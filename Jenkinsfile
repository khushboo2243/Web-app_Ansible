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
                withCredentials([sshUserPrivateKey(credentialsId: '5f2efc63-a4f8-4c24-bf09-3f1a346cbdcf')]) {
    // some block
}
       }
     }
    stage('Ping') {
      steps {
          
          sh 'ansible -vvvv all -m ping'
          
      }      
    }

  } 

}
