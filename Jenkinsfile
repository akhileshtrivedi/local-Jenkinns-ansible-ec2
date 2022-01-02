  pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git branch: 'main', credentialsId: 'github',
                url: 'https://github.com/akhileshtrivedi/local-Jenkinns-ansible-ec2'
            }
            
        }
       stage('Execute Ansible Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'playbook.yml'
            }
            
        }
     }
}
