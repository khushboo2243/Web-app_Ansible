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
          
          sh 'ansible -vvvv all -m ping'
          
      }      
    }

  } 

}
