pipeline {
    agent {
        docker {
            image "ruby"
            args "--link selenium"
        }
    }
    stages {
        stage("Build") {
            steps {
                sh "bundle install"
                sh "cucumber"
            }
        }
    }
}