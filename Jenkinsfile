pipeline {
    agent { label 'workstation'}

    options {
        ansiColor('xterm')
    }

    stages {

        stage('code quality'){
            steps {
                sh 'sonar-scanner -Dsonar.host.url=http://172.31.20.139:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=frontend -Dsonar.qualitygate.wait=true'
            }
        }

        stage('Release'){
            steps {

                echo 'CI'
            }
        }
    }
}

