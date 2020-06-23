pipeline {
    agent any
    parameters {
        string(name: 'Person', defaultValue: 'Anju', description: 'Who are you?')
    }
    stages {
        stage('Hi') {
            steps {
                echo "${params.Person} World!"
            }
        }
        stage('Greet the guy') {
            steps {
                echo '> Deploying the application ...'
                sh "ansible-playbook -vv main.yml --extra-vars username=${params.Person}"
            }
        }
    }
}
