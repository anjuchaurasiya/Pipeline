pipeline {
    agent any
    parameters {
        string(name: 'Person', defaultValue: 'Anju', description: 'Who are you?')
    }
    stages {
        stage('Greet the guy') {
            steps {
                echo '> Deploying the application ...'
                ansiblePlaybook(
                    playbook: 'main.yml'
                    extraVars: [
                        username: "${params.Person}",
                   ]     
                )
            }
        }
    }
}
