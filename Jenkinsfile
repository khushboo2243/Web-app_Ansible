pipeline {

  agent any
  
  stages {

   stage('Checkout') {
      steps {
        checkout scm
        
      }
    }
    
    stage('Ping') {
      steps {
          
          sh 'sudo ansible all -m ping'
          
      }      
    }

  } 

}
