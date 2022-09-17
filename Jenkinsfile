pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                checkout scm
                sh 'echo Hello'
                sh '/opt/apache-maven-3.8.1/bin/mvn validate'
            }
        }
        stage('Build') {
            steps {
                sh 'docker pull gesellex/trufflehog'
                sh 'docker run gesellix/trufflehog --json https://github.com/devopssecure/webapp.git > trufflehog'
            }
        }
    }
}
