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
   
        sh 'sudo ansible all -i /etc/ansible/hosts --private-key=/var/lib/jenkins/workspace/AnsibleJenkins/id_rsa -m ping -u opc -v'
          
      }      
    }
    
    stage('Execute'){
      
      steps{
        
        sh'ansible-playbook -i /etc/ansible/hosts --private-key=/var/lib/jenkins/workspace/AnsibleJenkins/id_rsa -s /home/opc/ansible/main.yaml'
      }
    }

  } 

}
