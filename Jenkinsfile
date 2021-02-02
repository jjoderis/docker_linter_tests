pipeline {
    agent none

    stages {
        stage("lint") {
            agent docker {
                image 'hadolint/hadolint'
                args 'cp Dockerfile /'
            }
            steps {
                sh 'hadolint /Dockerfile'
            }
        }
    }

}