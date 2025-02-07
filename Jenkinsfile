pipeline {
    agent any
    stages {
        stage('SSH TO RANCHER SERVER') {

            steps {
                script {
                    sh '''
                        ssh user@rancher-server "ls; pwd; free -h"
                    '''
                }
            }
        }
    }
}
