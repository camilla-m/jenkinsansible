pipeline {
    agent any
    parameters {
        string(name: 'NAMEINST', defaultValue: 'jenkins', description: 'Nome da instalação a ser criada')
    }
    stages {
        stage('Deploying Ansible') {
            steps {
                ansible-playbook playbook-inicial.yml --extra-vars="nameinvault=${params.NAMEINST}"
            }
        }
    }
}