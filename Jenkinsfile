pipeline {
    agent any
 
    stages {
        stage('Deploy') {
            steps {
                echo '> Deploying the application ...'
                ansiblePlaybook(
                    playbook: 'main.yml'
                )
            }
        }
    }
}
