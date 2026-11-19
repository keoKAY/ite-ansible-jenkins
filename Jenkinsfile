pipeline{
    agent any
    stages{
        stage("Basic"){
            steps{
                sh """
                ansible --version 
                ansible localhost -m ping 
                ansible stag-server -m ping 
                """
            }
        }

        stage("Deploy Spring"){
            steps{
                sh """
                 ansible-playbook playbooks/fileupload-main.yaml
                """
            }
        }
    } 
}