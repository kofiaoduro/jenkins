pipeline {
    agent { label 'docker-agent' }  // Use the label of your pre-configured agent
    stages {
        stage('Build') {
            steps {
                echo "Building branch: $GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
                sh(script: 'docker compose build')  // Run Docker Compose build on the agent
            }
        }
    }
}
