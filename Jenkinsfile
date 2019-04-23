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
   
        sh ' sudo ansible all -i /etc/ansible/hosts --private-key=/var/lib/jenkins/workspace/AnsibleJenkins/.ssh/id_rsa -m ping -u opc -v'
          
      }      
    }
    
    stage('Execute'){
      
      steps{
        
        sh 'sudo ansible-playbook -s /var/lib/jenkins/workspace/AnsibleJenkins/main.yaml '
      }
    }

  } 

}
