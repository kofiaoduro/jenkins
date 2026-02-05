pipeline {
    agent { label 'docker-agent-test' }  // Use the label of the agent you created

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

