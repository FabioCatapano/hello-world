pipeline {

    agent {
        node {
            label 'master'
        }
    }

    stages {

        stage(' Unit Testing') {
            steps {
                sh """
                echo "Running Unit Tests"
                echo "Ciao"
                echo "Riciao"
                """
            }
        }

        stage('Code Analysis') {
            steps {
                sh """
                echo "Running Code Analysis"
                """
            }
        }

        stage('Build Deploy Code') {
            when {
                branch 'develop'
            }
            steps {
                sh """
                echo "Building Artifact"
                """

                sh """
                echo "Deploying Code"
                """
            }
        }

    }   
}
