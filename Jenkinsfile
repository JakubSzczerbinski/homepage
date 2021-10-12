pipeline {
    agent any
    stages {
        stage('deploy') {
            steps {
                withCredentials([string(credentialsId: 'HOMESERVER_ADRESS', variable: 'HOMESERVER_IP')]) {
                    sh 'scp -r * root@$HOMESERVER_IP:/var/www/html/
                }
            }
        }
    }
}