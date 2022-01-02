  pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git branch: 'main', credentialsId: 'github',
                url: 'https://github.com/akhileshtrivedi/jenkins-ansible'
            }
            
        }
       stage('Execute Ansible Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'playbook.yml'
            }
            
        }
     }
}
