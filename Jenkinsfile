pipeline {
    agent {
        label 'nu-checker'
    }
    stages {
        stage('run scan') {
            steps {
                // Your build steps here
                container('nu-checker') {
                  sh 'vnu'
                }
            }
        }

    }
}